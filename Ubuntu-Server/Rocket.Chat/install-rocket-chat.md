# Install Rocket.Chat

## Install with Snap
```bash
sudo snap install rocketchat-server
```

## Install with Docker
```bash
sudo apt update && sudo apt upgrade
sudo apt install -y git
curl -fsSL https://get.docker.com/ | sh
sudo apt install docker-compose

sudo git clone https://github.com/RocketChat/Rocket.Chat.git
cd Rocket.Chat
sudo vim docker-compose.yml

sudo docker-compose up -d

sudo curl localhost:3000
```