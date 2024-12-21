# 🌟 Hyprland Ubuntu Dotfiles

<div align="center">

![Hyprland Logo](https://raw.githubusercontent.com/hyprwm/Hyprland/main/assets/header.png)

[![Stars](https://img.shields.io/github/stars/yourusername/dotfiles?color=yellow&style=for-the-badge)](https://github.com/yourusername/dotfiles/stargazers)
[![License](https://img.shields.io/github/license/yourusername/dotfiles?color=green&style=for-the-badge)](./LICENSE)
[![Issues](https://img.shields.io/github/issues/yourusername/dotfiles?color=red&style=for-the-badge)](https://github.com/yourusername/dotfiles/issues)

*A modern, highly customized environment for Ubuntu 24.04 with Hyprland*

[Features](#-features) •
[Prerequisites](#-prerequisites) •
[Installation](#-installation) •
[Customization](#-customization) •
[Troubleshooting](#-troubleshooting) •
[Gallery](#-gallery)

</div>

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Prerequisites](#-prerequisites)
- [Installation](#-installation)
- [Configuration](#-configuration)
- [Customization](#-customization)
- [Keybindings](#-keybindings)
- [Troubleshooting](#-troubleshooting)
- [Gallery](#-gallery)
- [Contributing](#-contributing)
- [License](#-license)

## 🌟 Overview

Welcome to my carefully crafted dotfiles repository! This collection is designed to transform your Ubuntu 24.04 system into a modern, efficient, and aesthetically pleasing development environment using Hyprland as the Wayland compositor. These configurations prioritize both functionality and visual appeal, creating a seamless and productive workspace.

### 🎯 Design Philosophy

- **Minimalism**: Clean and distraction-free interface
- **Efficiency**: Optimized workflows and keyboard-centric controls
- **Aesthetics**: Modern and cohesive design language
- **Productivity**: Carefully selected tools and configurations

## ✨ Features

### 🖥️ Core Components

- **Hyprland**: A dynamic tiling Wayland compositor
- **Waybar**: Highly customizable status bar
- **Kitty**: Modern, feature-rich terminal emulator
- **Neovim**: Extensible, powerful text editor
- **Fish**: User-friendly shell with smart features
- **Rofi**: Application launcher and window switcher
- **Dunst**: Lightweight notification daemon

### 🎨 Visual Enhancements

- Custom color scheme based on [Catppuccin](https://github.com/catppuccin/catppuccin)
- Carefully selected Nerd Fonts for icons and text
- Smooth animations and transitions
- Consistent theming across all applications

### 🛠️ Developer Tools

- Preconfigured Neovim with LSP support
- Git integration and customizations
- Development-focused terminal utilities
- Smart code completion and snippets

## 📋 Prerequisites

### System Requirements

- Ubuntu 24.04 LTS
- Wayland-compatible GPU
- 4GB RAM (minimum)
- 20GB free disk space

### Required Packages

```bash
sudo apt update && sudo apt install -y \
    hyprland \
    waybar \
    kitty \
    neovim \
    fish \
    rofi \
    dunst \
    git \
    fonts-nerd-fonts-complete \
    spicetify-cli \
    brightnessctl \
    network-manager \
    pulseaudio \
    pavucontrol \
    bluez \
    blueman
```

## 🚀 Installation

### 1. Backup Existing Configurations

```bash
# Create backup directory
mkdir -p ~/.config/backup

# Backup existing configs
for dir in hypr waybar kitty nvim fish rofi dunst; do
    [ -d ~/.config/$dir ] && cp -r ~/.config/$dir ~/.config/backup/
done
```

### 2. Clone Repository

```bash
# Clone dotfiles
git clone https://github.com/yourusername/dotfiles.git ~/.dotfiles

# Create necessary directories
mkdir -p ~/.config ~/.local/share/fonts
```

### 3. Install Configurations

```bash
# Copy configurations
cd ~/.dotfiles
./install.sh

# Set fish as default shell
chsh -s $(which fish)
```

### 4. Install Fonts

```bash
# Copy fonts
cp -r ~/.dotfiles/fonts/* ~/.local/share/fonts/
fc-cache -f -v
```

### 5. Apply Configurations

```bash
# Reload Hyprland
hyprctl reload

# Restart Waybar
killall waybar && waybar &
```

## ⚙️ Configuration

### Directory Structure

```
~/.config/
├── hypr/
│   ├── hyprland.conf
│   ├── autostart.conf
│   └── themes/
├── waybar/
│   ├── config
│   └── style.css
├── kitty/
│   └── kitty.conf
├── nvim/
│   └── init.vim
└── fish/
    └── config.fish
```

## 🎨 Customization

### Hyprland Configuration

Edit `~/.config/hypr/hyprland.conf`:

```bash
# Example customizations
monitor=eDP-1,1920x1080@60,0x0,1
input {
    kb_layout = us
    follow_mouse = 1
}
```

### Waybar Customization

Edit `~/.config/waybar/config`:

```json
{
    "position": "top",
    "modules-left": ["hyprland/workspaces"],
    "modules-center": ["clock"],
    "modules-right": ["pulseaudio", "network", "battery"]
}
```

### Theme Configuration

```bash
# Set GTK theme
gsettings set org.gnome.desktop.interface gtk-theme 'Catppuccin'

# Set icon theme
gsettings set org.gnome.desktop.interface icon-theme 'Papirus'
```

## ⌨️ Keybindings

### Window Management

| Keybinding | Action |
|------------|--------|
| `SUPER + Enter` | Launch terminal |
| `SUPER + Q` | Close window |
| `SUPER + Space` | Launch Rofi |
| `SUPER + [1-9]` | Switch workspace |
| `SUPER + Shift + [1-9]` | Move window to workspace |

### System Controls

| Keybinding | Action |
|------------|--------|
| `SUPER + L` | Lock screen |
| `SUPER + Shift + Q` | Logout |
| `SUPER + Shift + R` | Reload config |
| `SUPER + P` | Power menu |

## 🔧 Troubleshooting

### Common Issues

#### Hyprland Won't Start

1. Check logs:
```bash
cat ~/.local/share/hyprland/hyprland.log
```

2. Verify Wayland compatibility:
```bash
echo $XDG_SESSION_TYPE
```

#### Missing Fonts

Install Nerd Fonts:
```bash
sudo apt install fonts-nerd-fonts-complete
```

#### Waybar Issues

Reset Waybar:
```bash
killall waybar
rm -rf ~/.cache/waybar/*
waybar &
```

## 📸 Gallery

<div align="center">

![Screenshot 1](screenshots/desktop.png)
*Clean Desktop*

![Screenshot 2](screenshots/terminal.png)
*Terminal Setup*

![Screenshot 3](screenshots/development.png)
*Development Environment*

</div>

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Hyprland](https://github.com/hyprwm/Hyprland) team
- [Catppuccin](https://github.com/catppuccin/catppuccin) theme creators
- [Waybar](https://github.com/Alexays/Waybar) contributors
- The entire Linux riceing community

## 📬 Contact

- GitHub: [@yourusername](https://github.com/yourusername)
- Reddit: [u/yourusername](https://reddit.com/u/yourusername)
- Discord: yourusername#0000

---

<div align="center">

Made with ❤️ by [Your Name]

If you find this helpful, consider starring the repository ⭐

</div>