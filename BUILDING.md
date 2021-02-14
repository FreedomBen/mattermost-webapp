# Build Instructions (WIP)

## Ubuntu 20.04

### Ubuntu 20.04 dev packages:

```sh
apt install -y \
    vim \
    git \
    tmux \
    htop \
    mosh
```

### Ubuntu 20.04 build packages:

```sh
apt install -y \
    nodejs \
    npm \
    docker \
    docker-compose \
    make \
```

### Ubuntu 20.04 build steps:

#### Install golang

```sh
curl -LO https://get.golang.org/$(uname)/go_installer && chmod +x go_installer && ./go_installer && rm go_installer
source $HOME/.bash_profile
```

#### Build the stuff

Docs:  https://developers.mattermost.com/extend/customization/webapp/

git clone https://github.com/FreedomBen/mattermost-webapp.git
cd mattermost-webapp/
make build
cd dist
tar -cvf dist.tar *

# Then on server deployment:
cd ~/mattermost/client && rm -rf *
tar -xvf dist.tar
```

## Fedora

### Fedora 33 dev packages:

```sh
dnf install -y
    git \
    tmux \
    vim \
    mosh \
    htop
```

### Fedora 33 Build packages required:

```sh
dnf install -y
    nodejs \
    golang \
    docker \
    docker-compose \
    make \
    
```
