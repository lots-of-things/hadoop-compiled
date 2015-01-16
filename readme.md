    1  sudo nano /etc/init/tty1.conf 
    2  sudo reboot
    3  exit
    4  sudo apt-get install java-openjdk
    5  sudo apt-get install java-7-openjdk
    6  sudo apt-get install openjdk-7-jdk
    7  sudo apt-get install ssh
    8  sudo apt-get install git
    9  ssh-keygen -t rsa -P '' -f ~/.ssh/id_rsa
   10  cat .ssh/id_rsa.pub >> .ssh/authorized_keys
   11  ssh localhost
   12  cd /usr/local/
   13  git clone https://github.com/lots-of-things/hadoop-compiled.git
   14  sudo git clone https://github.com/lots-of-things/hadoop-compiled.git
   15  ls
   16  mv hadoop-compiled/hadoop/ hadoop/
   17  sudo mv hadoop-compiled/hadoop/ hadoop/
   18  ls
   19  cd hadoop
   20  ls
   21  cd ..
   22  cd hadoop-compiled/
   23  ls
   24  cd ..
   25  rm -r hadoop-compiled/
   26  ls
   27  rm -rf hadoop-compiled/
   28  sudo rm -rf hadoop-compiled/
   29  ls
   30  cd hadoop/
   31  ls
   32  git status
   33  cd ..
   34  ls
   35  sudo rm -rf hadoop/
   36  ls
   37  sudo git clone https://github.com/lots-of-things/hadoop-compiled.git
   38  ls
   39  mv hadoop-compiled/ hadoop
   40  sudo mv hadoop-compiled/ hadoop
   41  cd hadoop/
   42  ls
   43  sudo mv hadoop/* .
   44  ls
   45  sudo rm -rf hadoop/
   46  git commit -m "ditched extra directory"
   47  sudo git commit -m "ditched extra directory"
   48  git config --global user.email "wmcfadd2@gmail.com"
   49  git config --global user.name "wmcfadden"
   50  sudo git commit -m "ditched extra directory"
   51  sudo git add *
   52  sudo git commit -m "ditched and fixed"
   53  git push origin master
   54  sudo git push origin master
   55  ls
   56  cd etc
   57  ls
   58  cd hadoop/
   59  ls
   60  nano mapred-site.xml
   61  sudo nano mapred-site.xml
   62  sudo nano yarn-site.xml
   63  cd ..
   64  ls
   65  git status
   66  git add -u
   67  sudo git add -u
   68  ls
   69  git status
   70  git commit -m "ready to roll"
   71  sudo git commit -m "ready to roll"
   72  sudo git push origin master
   73  cd ~
   74  nano .bashrc 
   75  cp .bashrc /usr/local/hadoop/
   76  sudo cp .bashrc /usr/local/hadoop/
   77  history
   78  exit
   79  history
   80  history > /usr/local/hadoop/readme.md
   81  sudo history > /usr/local/hadoop/readme.md
   82  cd /usr/local/hadoop/
   83  sudo history > readme.md
   84  nano readme.md
   85  sudo nano readme.md
   86  sudo history > readme.md
   87  cat history
   88  cp ~/.bash_history readme.md
   89  sudo cp ~/.bash_history readme.md
   90  git status
   91  git add *
   92  sudo git add *
   93  sudo git commit -m "real readme"
   94  sudo git push origin master
   95  cd ~
   96  history > readme.md
