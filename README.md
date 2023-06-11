![watch_me_build_blockchain_insurance_app](https://github.com/josuebatista/blockchainapp/assets/25143822/bddd6335-3cff-496c-8901-3889ff1e7649)
# Watch Me Build A Blockchain Insurance App (5 Videos)

## SECTION #1

Video # 1 - [Introduction and Google Cloud server setup](https://player.vimeo.com/video/355777539?h=1527f93fe5)

This video shows you how to create a brand new virtual machine (VM) on Google Cloud.  
To create your own free Google Cloud account, go to [https://cloud.google.com/free/](https://cloud.google.com/free/)  
To download PuTTY go to [https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)

## SECTION #2

Video # 2 - [Install Docker, Docker Compose, and Git](https://player.vimeo.com/video/355777916)

1. SET UP THE REPOSITORY

1.1. Update the apt package index:
```
$ sudo apt-get update
```

1.2. Install packages to allow apt to use a repository over HTTPS:
```
$ sudo apt-get install \
apt-transport-https \
ca-certificates \
curl \
gnupg-agent \
software-properties-common
```

1.3. Add Docker’s official GPG key:
```
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

1.4. Verify that you now have the key with the fingerprint 9DC8 5822 9FC7 DD38 854A E2D8 8D81 803C 0EBF CD88, by searching for the last 8 characters of the fingerprint.
```
$ sudo apt-key fingerprint 0EBFCD88
```

1.5. Set up the stable repository
```
$ sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```

2. INSTALL DOCKER ENGINE - COMMUNITY (CE)

2.1. Update the apt package index.
```
$ sudo apt-get update
```

2.2. Identify the candidate for installation
```
$ apt-cache policy docker-ce
```

2.3. Install the latest version of Docker Engine - Community and containerd (it installs git as well):
```
$ sudo apt-get install docker-ce docker-ce-cli containerd.io
```

2.4. Verify that Docker Engine - Community is installed correctly by running the hello-world image.
```
$ sudo docker run hello-world
```

2.5. Verify Docker version
```
$ sudo docker -v
```

3. INSTALL DOCKER COMPOSE

3.1. Download the current stable release of Docker Compose:
```
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.24.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

3.2. Set the permissions:
```
$ sudo chmod +x /usr/local/bin/docker-compose
```

3.3. Check the version:
```
$ docker-compose --version
```

## SECTION #3

Video # 3 - [Install Node.js, the Node.js Package Manager (NPM), and the Node.js Version Manager (NVM)](https://player.vimeo.com/video/355778293)

1. Refresh your local package index by typing:
```
$ sudo apt update
```

2. Install Node.js from the repositories:
```
$ sudo apt install nodejs
```

3. Install npm
```
$ sudo apt install npm
```

4. Install nvm
```
$ sudo apt-get install build-essential libssl-dev
$ curl -sL https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh -o install_nvm.sh
$ bash install_nvm.sh
$ source ~/.profile
$ nvm ls-remote
```

## SECTION #4

Video # 4 - [Install Python](https://player.vimeo.com/video/355777539)

1. Install Prerequisites
```
$ sudo apt-get update
$ sudo apt-get install build-essential checkinstall
$ sudo apt-get install libreadline-gplv2-dev libncursesw5-dev libssl-dev libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev
```

2. Download Python 2.7
```
$ cd /usr/src
$ sudo curl -o Python-2.7.16.tgz https://www.python.org/ftp/python/2.7.16/Python-2.7.16.tgz
$ sudo tar xzf Python-2.7.16.tgz
```

3. Compile Python Source
```
$ cd Python-2.7.16
$ sudo ./configure --enable-optimizations
$ sudo make altinstall
```

## SECTION #5

Video # 5 - [Run the Blockchain Insurance App](https://player.vimeo.com/video/356289383)

1. Clone the repository:
```
$ sudo git clone https://github.com/IBM/build-blockchain-insurance-app
```

2. Login using your docker hub credentials.
```
$ sudo docker login
```

3. Run the build script
```
$ cd build-blockchain-insurance-app
$ sudo ./build_ubuntu.sh
```

4. Check the status of installation using command:
```
$ sudo docker logs web
```
