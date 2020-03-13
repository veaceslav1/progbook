# Docker installation

Note: on windows install virtualbox and run on it ubuntu. Install docker on ubuntu.

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

3. Install compose:

  ```bash
  sudo curl -L "https://github.com/docker/compose/releases/download/1.25.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
  sudo chmod +x /usr/local/bin/docker-compose
  ```
