# Home Server

Welcome to your DIY home server hub! This repository offers a set of Docker Compose configurations for easily deploying and managing a variety of open-source services like Immich, Jellyfin, Navidrome, FileBrowser, FreshRSS, and more. Whether you’re setting up media streaming, file management, or infrastructure services like Tailscale, this setup helps you quickly spin up your server on your own hardware.

Key Features:

* Ready-to-go setups for popular services.
* Fixed Docker image tags for stable rollbacks in case of issues.
* Customizable volume locations and user credentials – make sure to adjust these to fit your environment.
* Best practices for sharing resources between containers.

Start by following the installation steps to get up and running quickly. Enjoy the flexibility and control of your self-hosted environment.

## Playbook for new system install

### OH-MY-ZSH

What is [oh my zsh](https://ohmyz.sh/)?


```bash
sudo apt install curl wget git zsh
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
nano ~/.zshrc
```

### Docker compose

[Tutorial](https://linuxvox.com/blog/install-dockercompile-ubuntu-server/)

Make sure normal user can use docker
```bash
sudo usermod -aG docker ${USER}
```

To use the repo, navigate to it's root.
```bash
docker compose up -d
```

### Git

Clone git and remember credentials
```bash
git config credential.helper store
git config --global user.name "Tom Waits"
git config --global user.email "xxx@yyy.zzz"
git config --global user.password 'ghp_jadiejadieja'
```
