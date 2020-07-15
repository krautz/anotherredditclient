# ARC - Another Reddit Client
Project to create a new reddit client, with some features lacking on official one, such as:
 - Persisting posts (They will be saved even if they are deleted from the subreddit)
 - Filtering the feed with desired subreddits
 - Enhanced UI/UX

## Configuration

In order to be able to run this project, expose the following environment variables on your host (or set them on the docker-compose.yml file)
```
export REDDIT_MEDIATOR_USER_USERNAME=<YOUR REDDIT USER>
export REDDIT_MEDIATOR_USER_PASSWORD=<YOUR REDDIT USER PASSWORD>
export REDDIT_MEDIATOR_APP_ID=<YOUR REDDIT APP ID>
export REDDIT_MEDIATOR_APP_SECRET=<YOUR REDDIT APP SECRET>
```

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
