# Dotfiles & Configs

## Table of Contents
- [Software](#software)


## Tiling Manager
- [Qtile](.config/qtile/README.md)

## Software
### Basic utilities
```sh
# build essentials
sudo pacman -S git vim make automake cmake

# package manager
sudo pacman -S yay snapd npm stack
sudo systemctl enable snapd
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

```sh
sudo pacman -S ttf-dejavu ttf-liberation noto-fonts noto-fonts-emoji noto-fonts-extra
```
### Apps
- [Slack](https://snapcraft.io/slack)

```sh
sudo pacman -S alacritty ruby go
```
- [Spacemacs](docs/spacemacs.md)
- Python
```sh
# pip
sudo pacman -S python-pip pyenv
# pipx
pip install pipx
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
```
