# Home Server

This repository provides a ready-to-go collection of Docker Compose configurations for running a variety of open-source services on your own hardware. Whether you're looking to stream media, manage files, aggregate RSS feeds, or integrate with Tailscale, this repo has you covered. With easy-to-follow setup instructions and best practices for sharing resources between containers, you'll have your self-hosted server up and running in no time.

Get started by following the installation guide, and enjoy the flexibility of a fully customizable, self-hosted environment!

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
