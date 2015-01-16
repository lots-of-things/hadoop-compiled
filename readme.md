This is my working version of a hadoop distribution that is setup to run my own cluster.  If you do a fresh install of Ubuntu 14.04 and then follow these instructions you'll have a single node distribution.

1) I'm setting up an automatic login so that my nodes will boot when I turn the machine on.  You do this by changing the tty1 file.  Just add "-a <username>" at the end of the last line ("exec /sbin/getty -8 38400 tty")

    sudo nano /etc/init/tty1.conf 
    exec /sbin/getty -8 38400 tty -a doopy
    
2) Install java ssh and git.

    sudo apt-get install openjdk-7-jdk ssh git
    
3) Setup passwordless ssh

    ssh-keygen -t rsa -P '' -f ~/.ssh/id_rsa
    cat .ssh/id_rsa.pub >> .ssh/authorized_keys
    ssh localhost
    exit
    
4) Clone this git repository

    cd /usr/local/
    sudo git clone https://github.com/lots-of-things/hadoop-compiled.git hadoop
    
5) Replacing .bashrc is optional, but I do it so that I can run things easier

    cp .bashrc ~
    
    
