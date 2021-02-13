# Install Docker in Ubuntu

sudo apt-get install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository  "deb [arch=amd64] https://download.docker.com/linux/ubuntu  $(lsb_release -cs) stable"
sudo apt-get update
sudo apt-get -y install docker-ce


# Check if Docker is Running

sudo systemctl status docker

# Running Docker without Sudo

sudo usermod -aG docker ${USER}
su - ${USER}

# Running Docker Compose

sudo curl -L https://github.com/docker/compose/releases/download/1.17.0/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose

# Check if Docker Compose Installed

docker-compose --version

# Cloning the repo

git clone https://github.com/jitsi/docker-jitsi-meet && cd docker-jitsi-meet
cp env.example .env
./gen-passwords.sh
 
 Edit the .env file as per requirements
 
 mkdir -p ~/.jitsi-meet-cfg/{web/letsencrypt,transcripts,prosody/config,prosody/prosody-plugins-custom,jicofo,jvb,jigasi,jibri}

# Building the docker images

docker-compose up -d

# List the docker containers

docker ps
