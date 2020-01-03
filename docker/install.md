# Docker installation

Note: on windows install virtualbox and run on it ubuntu. Install docker on ubuntu.

Visit [docker installation](https://docs.docker.com/install/linux/docker-ce/ubuntu/) instructions.

## Install from repository

    ```bash
    sudo apt update

    sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common

    # add docker's gpg:
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

    # append dockers repository link
    sudo add-apt-repository \
    "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
    $(lsb_release -cs) \
    stable"

    sudo apt update

    # install docker and tools:
    sudo apt-get install docker-ce docker-ce-cli containerd.io
    ```

## Install docker-compose:

    ```bash
    sudo curl -L "https://github.com/docker/compose/releases/download/1.25.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

    sudo chmod +x /usr/local/bin/docker-compose
    ```
    
## Installing using script

1. Download installation script and run it:

  ```bash
  cd ~
  curl -fsSL https://get.docker.com -o get-docker.sh
  sudo sh get-docker.sh
  ```
2. Append your username to docker group:

  ```bash
  sudo usermod -aG docker <your-user-name>
  ```
