# 🌟 Hyprland Ubuntu Dotfiles Setup Guide

## Introduction

This repository contains a collection of dotfiles optimized for a clean, efficient Wayland setup using Hyprland, Waybar, Kitty, Neovim, Fish, and more. These dotfiles are designed to provide a fully functional, aesthetically pleasing, and efficient environment for users of Ubuntu 24.04 with Wayland compositors. The setup aims to enhance productivity and streamline your environment. 🚀

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

Run this command to clone the repository:

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

To create backups of your existing configurations, run these commands:

```bash
mkdir -p ~/.config/backup
cp -r ~/.config/hypr ~/.config/backup/
cp -r ~/.config/waybar ~/.config/backup/
cp -r ~/.config/kitty ~/.config/backup/
```

#### Important Notes:
This backup procedure will create a safe copy of your existing Hyprland, Waybar, and Kitty configurations.

### Step 4: Apply the Dotfiles

Now that the repository is cloned, and your backups are safely stored, it's time to apply the dotfiles to your system. You can do this by copying the configuration files from the cloned repository to your ~/.config directory. 📂➡️📁

Run the following command to apply the dotfiles:

```bash
cp -r ~/dotfiles/.config/* ~/.config/
```

#### Important Notes:
- This command will replace your current configuration files with those from the repository. Ensure that your backups are safely stored in case you need to revert.
- These dotfiles include configurations for Hyprland, Waybar, Kitty, Neovim, Fish, and more.

### Step 5: Set Fish as the Default Shell

The dotfiles repository uses Fish as the default shell. If you're not using Fish already, you need to set it as your default shell by running the following command:

```bash
chsh -s /usr/bin/fish
```

#### Important Notes:
The chsh command changes your default shell. Fish is designed to be user-friendly, with features like autosuggestions and syntax highlighting. 🐟

After setting Fish as the default shell, restart your terminal or log out and log back in to see the changes.

### Step 6: Restart Your System

Once you've applied the dotfiles and set Fish as your default shell, it's recommended to restart your system. This will ensure that all environment variables, shell changes, and compositor configurations are loaded correctly. 🔄

To restart your system, run:

```bash
sudo reboot
```

#### Important Notes:
Restarting your system ensures that Hyprland, Waybar, and other system changes take effect. It will also start the system with your new configuration.

## ⚠️ Warnings & Notes

- **Backup**: Always back up your existing configurations before applying new dotfiles. If something goes wrong, you can restore your old settings.
- **Customization**: These configurations are designed to be a general starting point. You may need to adjust specific settings based on your hardware and personal preferences.
- **Troubleshooting**: If Hyprland does not start or behaves unexpectedly, check the logs in the following file:
  ```bash
  cat ~/.config/hypr/hyprland.log
  ```
- **Neovim Configuration**: The dotfiles include a basic configuration for Neovim. If you're new to Neovim, make sure to explore the documentation for further customization options. You can modify the `~/.config/nvim/init.vim` file to fine-tune your Neovim setup.

## 🎨 Customization (Optional)

You can customize the configurations to match your specific preferences:

- **Hyprland**: Adjust the Hyprland configuration file located at `~/.config/hypr/hyprland.conf` to fit your monitor layout, input devices, and compositor settings. 🖥️
- **Waybar**: The Waybar configuration can be found in `~/.config/waybar/config`. You can modify its appearance, the modules displayed, and how it interacts with other system elements. 🌈
- **Kitty**: To adjust Kitty terminal settings, open the `~/.config/kitty/kitty.conf` file and make changes based on your preferences. 🖱️
- **Neovim**: For Neovim, you can further customize your editor by installing plugins and modifying the settings in the init.vim file. ✨

## 🛠️ Troubleshooting

### 1. Hyprland Won't Start
- Check the Hyprland log file located at `~/.config/hypr/hyprland.log` for any error messages or warnings.
- Ensure your display server (Wayland) is properly configured.

### 2. Waybar Doesn't Display Correctly
- Check the Waybar configuration in `~/.config/waybar/config`. Some modules might need to be adjusted to fit your screen resolution or personal preferences.

### 3. Kitty Terminal Shows No Icons
Make sure you have Nerd Fonts installed. If not, you can install them by running:
```bash
sudo apt install fonts-nerd-fonts-complete
```

### 4. Fish Shell Not Working Properly
If the Fish shell isn't showing as expected, ensure it is installed and set as the default shell by running:
```bash
chsh -s /usr/bin/fish
```

## 🎉 Conclusion

By following this guide, you should now have a fully functional, aesthetically pleasing, and highly efficient Hyprland + Ubuntu 24.04 setup using these dotfiles. This environment is designed to streamline your workflow, improve productivity, and provide a smooth user experience. 🌟

Enjoy your new setup! 🎉

---

Let me know if you need further assistance or adjustments!