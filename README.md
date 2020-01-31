# my-laravel-docker-template
My laravel docker template

## Install on Ubuntu 18, 19
### follow these instructions: https://www.digitalocean.com/community/tutorials/como-instalar-e-usar-o-docker-no-ubuntu-18-04-pt
```
  sudo apt update
  sudo apt install apt-transport-https ca-certificates curl software-properties-common
  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
  sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
  sudo apt update
  sudo apt install docker-ce
  sudo systemctl status docker
  sudo usermod -aG docker ${USER}
  su - ${USER}
  id -nG
```

#### run all containers in background (flag: -d)
> docker-compose up -d

#### artisan
> docker-compose exec app php artisan migrate --seed

#### create a virtual host
> echo "127.0.0.1 mysite.local" >> /etc/hosts

#### kill all containers
> docker kill $(docker ps -q) 
