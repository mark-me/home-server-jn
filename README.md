# Home Server

Welcome to your DIY home server hub! This repository provides a set of Docker Compose configurations designed to help you deploy and manage a variety of open-source services on an Ubuntu 24.04 Server. From media streaming with Jellyfin and Navidrome to file management with FileBrowser, this setup has you covered. Do you want a home-assistant compose?

### :key: Key Features:

* Ready-to-go setups for services I use and like.
* Fixed Docker image tags for stable rollbacks in case of issues.
* Customizable volume locations and user credentials – make sure to adjust these to fit your environment.
* Best practices for sharing resources between containers.

Start by following the installation steps to get up and running quickly. Enjoy the flexibility and control of your self-hosted environment.

### :stew: Add ingredients

My go-to place for usable and reliable home-server stuff is [linuxserver.io](https://www.linuxserver.io/), where you can find loads of docker images where each I've tried is reliable.

### :question: Requests

If you'd like to integrate Home Assistant into your self-hosted setup for smart home automation, or something else, let me know! Home Assistant can be easily added to this environment, and I can provide a  Docker Compose configuration to get you started.

:email: [Contact me](mailto:mark.zwart@pobox.com) to discuss how to best integrate Home Assistant with your existing services.

##  :rocket: Playbook for new system install

### :computer: oh-my-zsh!

What is [oh my zsh](https://ohmyz.sh/)?

Adds plugins:

* [Syntax highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
* [Suggests commands as you type based on history and completions](https://github.com/zsh-users/zsh-autosuggestions)


```bash
sudo apt install curl wget git zsh
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
nano ~/.zshrc
```

Add/change ~/.zshrc
```
ZSH_THEME="lukerandall"
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
```

### :whale: Docker compose

[Tutorial](https://linuxvox.com/blog/install-dockercompile-ubuntu-server/)

Make sure normal user can use docker
```bash
sudo usermod -aG docker ${USER}
```

To use the repo, navigate to it's root.
```bash
docker compose up -d
```

### :clock1: Git

Clone git and remember credentials
```bash
git config credential.helper store
git config --global user.name "Tom Waits"
git config --global user.email "xxx@yyy.zzz"
git config --global user.password 'ghp_jadiejadieja'
```
