# ubuntu_ansible_docker_compose

A docker compose project to create a docker image with ubuntu and ssh daemon

# dependencies

```
sudo mkdir -p ~/.docker/cli-plugins/
sudo curl -SL https://github.com/docker/compose/releases/download/v2.3.3/docker-compose-linux-x86_64 -o ~/.docker/cli-plugins/docker-compose
chmod +x ~/.docker/cli-plugins/docker-compose
```

# clone from git
```
sudo apt-get install -y git

‌sudo ‌git init
sudo git clone https://github.com/ansibleguy76/ubuntu_ansible_docker_compose.git
cd ubuntu_ansible_docker_compose
```

# build the docker image

```
docker build -t ubuntu-ansible-sshd .
```


# launch docker compose
```
docker-compose up -d
```

note : some flavors of dockercompose is run without a dash
```
docker compose up -d
```

2 images will launch, that you can ssh to.  

to stop the docker images use
```
docker-compose down
or
docker compose down
```