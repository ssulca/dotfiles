# Dotfiles & Configs

## Table of Contents
- [Tiling Manager](#tiling-manager)
- [Software](#software)

## Tiling Manager
- [Qtile](.config/qtile/README.md)

## Software
### Basic utilities
```sh
# build essentials
sudo pacman -S git vim make automake cmake fakeroot patch

# package manager
sudo pacman -S yay snapd npm
sudo systemctl enable --now snapd.socket
sudo ln -s /var/lib/snapd/snap /snap
sudo systemctl start snapd
```

### Laptop utilities (Optional)
```sh
# Optimize Linux Laptop Battery Life
sudo pacman -S tlp
sudo systemctl enable tlp
sudo systemctl start tlp
```

### Fonts, theming and GTK
- Fonts
```sh
sudo pacman -S ttf-dejavu ttf-liberation noto-fonts noto-fonts-emoji noto-fonts-extra
```

- Zsh
```sh
sudo pacman -S zsh
```

- [Oh My Zsh](https://github.com/ohmyzsh/ohmyzsh/)
```sh
git clone https://github.com/ohmyzsh/ohmyzsh.git ~/.oh-my-zsh
cp ~/.zshrc ~/.zshrc.orig
cp .zshrc ~/.zshrc
```

- Zsh Plugins
  - [zsh-completions](https://github.com/zsh-users/zsh-completions)
  - [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
  - [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
  - [powerlevel10k](https://github.com/romkatv/powerlevel10k)

### Apps
- [Slack](https://snapcraft.io/slack)
- [Code](https://snapcraft.io/code)

```sh
sudo pacman -S alacritty ruby go
```
- [Spacemacs](docs/spacemacs.md)
- Python
```sh
# pip and pipx
sudo pacman -S pyenv python-pip python-pipx
# pipx packages
pipx install poetry pre-commit
```
- Latex
```sh
sudo pacman -S texlive-core texlive-bin texlive-bibtexextra \
    texlive-fontsextra texlive-formatsextra texlive-langextra \
    texlive-latexextra texlive-pictures texlab
```
- Virtualization
```sh
# docker
sudo pacman -S docker docker-compose
# docker linter
yay -S hadolint
# kubernetes
sudo pacman -S helm kubectl
# k3d
yay -S rancher-k3d-bin
```
