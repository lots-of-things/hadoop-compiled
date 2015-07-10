This is my working version of a hadoop distribution that is setup to run my own cluster.  If you do a fresh install of Ubuntu 14.04 and then follow these instructions you'll have a single node distribution.  I made my login account doopy and that's what I use below.

1) I'm setting up an automatic login so that my nodes will boot when I turn the machine on.  You do this by changing the tty1 file.  Just add "-a <username>" at the end of the last line ("exec /sbin/getty -8 38400 tty")

    sudo nano /etc/init/tty1.conf 
    exec /sbin/getty -8 38400 tty -a doopy
    
2) Install java, ssh, and git.

    sudo apt-get install openjdk-7-jdk ssh git
    
3) Add a new user group and add doopy to it (just for kicks)

    sudo addgroup hadoop
    sudo usermod -g hadoop doopy
    
4) Setup passwordless ssh

    ssh-keygen -t rsa -P '' -f ~/.ssh/id_rsa
    cat .ssh/id_rsa.pub >> .ssh/authorized_keys
    ssh localhost
    exit
    
5) Clone my git repository

    cd /usr/local/
    sudo git clone https://github.com/lots-of-things/hadoop-compiled.git hadoop

6) Make yourself own the hadoop folder so you can change things 

    sudo chown -R doopy:hadoop hadoop
    
7) Adding to .bashrc is optional, but I do it so that I can run things easier

    cat hadoop/addToBash >> ~/.bashrc
    
8) Reboot to make sure everything works right

    sudo reboot
