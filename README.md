# 🌟 Hyprland Ubuntu Dotfiles Setup Guide

Welcome to the collection of dotfiles optimized for a clean, efficient Wayland setup using Hyprland, Waybar, Kitty, Neovim, Fish, and more. These dotfiles are designed to provide a fully functional, aesthetically pleasing, and efficient environment for users of Ubuntu 24.04 with Wayland compositors. The setup aims to enhance productivity and streamline your environment. 🚀

## 🛠️ Installation Guide

### Step 1: Install Dependencies

Before applying the dotfiles, ensure that you have all the required dependencies installed. These packages are necessary to get your system set up with the required software and utilities. ⚙️

Run the following command to install all the necessary dependencies:

```bash
sudo apt update
sudo apt install hyprland waybar kitty neovim fish rofi fonts-nerd-fonts-complete spicetify-cli git
```

#### Explanation of Installed Packages:

- **Hyprland**: A fast, efficient, and highly customizable Wayland compositor. 🌍
- **Waybar**: A customizable status bar for Wayland compositors like Hyprland. 📊
- **Kitty**: A fast and feature-rich terminal emulator. 💻
- **Neovim**: A modern, extensible version of Vim designed to be better, with enhanced features. 📝
- **Fish**: A user-friendly interactive shell that offers features like autosuggestions and syntax highlighting. 🐟
- **Rofi**: A window switcher and application launcher. 🖥️
- **Fonts**: Nerd fonts provide patched font icons for use with terminals and status bars. 🔤
- **Spicetify**: A tool for customizing Spotify's user interface. 🎶

### Step 2: Clone the Repository

Once you have the necessary dependencies installed, the next step is to clone the dotfiles repository to your home directory. 📂

```bash
git clone https://github.com/Matt-FTW/dotfiles.git ~/dotfiles
```

#### Important Notes:
Make sure that Git is installed on your system. If it is not installed, you can install it by running:

```bash
sudo apt install git
```

### Step 3: Backup Existing Configurations

Before applying the new configurations, it's essential to back up your existing dotfiles. This ensures you can easily revert to your previous setup if anything goes wrong. 💾

```bash
mkdir -p ~/.config/backup
cp -r ~/.config/hypr ~/.config/backup/
cp -r ~/.config/waybar ~/.config/backup/
cp -r ~/.config/kitty ~/.config/backup/
```

### Step 4: Apply the Dotfiles

Now that the repository is cloned, and your backups are safely stored, it's time to apply the dotfiles to your system. 📂➡️📁

```bash
cp -r ~/dotfiles/.config/* ~/.config/
```

#### Important Notes:
- This command will replace your current configuration files with those from the repository
- These dotfiles include configurations for Hyprland, Waybar, Kitty, Neovim, Fish, and more

### Step 5: Set Fish as the Default Shell

The dotfiles repository uses Fish as the default shell. Set it as your default shell by running: 🐟

```bash
chsh -s /usr/bin/fish
```

After setting Fish as the default shell, restart your terminal or log out and log back in to see the changes.

### Step 6: Restart Your System

Once you've applied the dotfiles and set Fish as your default shell, restart your system to ensure all changes take effect. 🔄

```bash
sudo reboot
```

## ⚠️ Warnings & Notes

- **Backup**: Always back up your existing configurations before applying new dotfiles
- **Customization**: These configurations are designed to be a general starting point
- **Troubleshooting**: Check Hyprland logs if issues occur:
  ```bash
  cat ~/.config/hypr/hyprland.log
  ```
- **Neovim Configuration**: Basic configuration included - explore documentation for customization

## 🎨 Customization (Optional)

### Configuration File Locations:

- **Hyprland**: `~/.config/hypr/hyprland.conf` - Adjust monitor layout, input devices, and compositor settings 🖥️
- **Waybar**: `~/.config/waybar/config` - Modify appearance, modules, and system interactions 🌈
- **Kitty**: `~/.config/kitty/kitty.conf` - Terminal preferences and settings 🖱️
- **Neovim**: `~/.config/nvim/init.vim` - Editor plugins and configuration ✨

## 🛠️ Troubleshooting

### 1. Hyprland Won't Start
- Check `~/.config/hypr/hyprland.log` for errors
- Verify Wayland configuration

### 2. Waybar Display Issues
- Review `~/.config/waybar/config`
- Adjust screen resolution settings

### 3. Missing Terminal Icons
Install Nerd Fonts:
```bash
sudo apt install fonts-nerd-fonts-complete
```

### 4. Fish Shell Issues
Verify installation and default shell:
```bash
chsh -s /usr/bin/fish
```

## 🎉 Conclusion

By following this guide, you should now have a fully functional, aesthetically pleasing, and highly efficient Hyprland + Ubuntu 24.04 setup using these dotfiles. This environment is designed to streamline your workflow, improve productivity, and provide a smooth user experience. 🌟

Enjoy your new setup! 🎊