# Install Docker in Ubuntu

1. ```sudo apt-get install apt-transport-https ca-certificates curl software-properties-common``` 
2. ```curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -``` 
3. ```sudo add-apt-repository  "deb [arch=amd64] https://download.docker.com/linux/ubuntu  $(lsb_release -cs) stable"``` 
4. ```sudo apt-get update``` 
5. ```sudo apt-get -y install docker-ce```


# Check if Docker is Running

6. ```sudo systemctl status docker```

# Running Docker without Sudo

7. ```sudo usermod -aG docker ${USER}```
8. ```su - ${USER}```

# Install Docker Compose

9. ```sudo curl -L https://github.com/docker/compose/releases/download/1.17.0/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose```
10. ```sudo chmod +x /usr/local/bin/docker-compose```

# Check if docker-compose installed successfully

11. ```docker-compose --version```

# Setup Jitsi Meet On Docker

12. ```git clone https://github.com/jitsi/docker-jitsi-meet && cd docker-jitsi-meet```
13. ```cp env.example .env```
14. ```./gen-passwords.sh```
 
 Edit the .env file as per requirements
 
 15. ```mkdir -p ~/.jitsi-meet-cfg/{web/letsencrypt,transcripts,prosody/config,prosody/prosody-plugins-custom,jicofo,jvb,jigasi,jibri}```

# Building the docker images

16. ```docker-compose up -d```

# List the docker containers

17. ```docker ps```
