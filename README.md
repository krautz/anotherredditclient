# Post Persister
Project to store reddit posts and sort them by tags

## Installation (assuming a CentOS7 minimal VM)

Enable Docker repository:
```
yum install yum-utils device-mapper-persistent-data lvm2 -y
yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
```

Install Docker
```
yum install docker-ce docker-ce-cli containerd.io -y
```

Ensure  it is and will be running
```
systemctl enable docker
systemctl start docker
```

Install docker-compose
```
curl -L "https://github.com/docker/compose/releases/download/1.23.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
```

Start projects containers:
```
docker-compose up -d
```
