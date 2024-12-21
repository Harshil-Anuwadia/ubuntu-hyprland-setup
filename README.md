Here's the updated README.md with all the content in plain text format as well as markdown:

# Hyprland Ubuntu Dotfiles

This repository contains a collection of dotfiles optimized for a clean, efficient Wayland setup using **Hyprland**, **Waybar**, **Kitty**, **Neovim**, **Fish**, and more, designed for **Ubuntu 24.04**. The goal of these dotfiles is to provide a fully functional, aesthetically pleasing, and efficient environment for users of Ubuntu with **Wayland** compositors.

This guide will walk you through the process of installing and setting up these dotfiles on your system, and help you customize your Ubuntu 24.04 environment to maximize your productivity and user experience.

---

## 🚀 Installation Guide

### 1. Install Dependencies

Before installing the dotfiles, ensure that you have all the required dependencies installed. Run the following command to install the necessary packages:

```bash
sudo apt update
sudo apt install hyprland waybar kitty neovim fish rofi fonts-nerd-fonts-complete spicetify-cli git

Explanation:

Hyprland: A Wayland compositor that is fast, efficient, and highly customizable.

Waybar: A customizable status bar for Wayland compositors like Hyprland.

Kitty: A fast and feature-rich terminal emulator.

Neovim: A text editor built to improve upon Vim with enhanced features and extensibility.

Fish: A user-friendly interactive shell that offers features like autosuggestions and syntax highlighting.

Rofi: A window switcher and application launcher.

Fonts: Nerd fonts provide patched font icons for use with terminals, status bars, and other tools.

Spicetify: A tool for customizing Spotify.


2. Clone the Repository

Clone the dotfiles repository to your home directory:

git clone https://github.com/Matt-FTW/dotfiles.git ~/dotfiles

Make sure that you have Git installed before running this command. You can install it via:

sudo apt install git

3. Backup Existing Configurations

It's always a good idea to back up your current configuration before making any changes. This allows you to revert to your previous setup if necessary.

mkdir -p ~/.config/backup
cp -r ~/.config/hypr ~/.config/backup/
cp -r ~/.config/waybar ~/.config/backup/
cp -r ~/.config/kitty ~/.config/backup/

4. Apply the Dotfiles

Now that you have the repository cloned and your backups in place, apply the dotfiles to your system:

cp -r ~/dotfiles/.config/* ~/.config/

This will replace existing configuration files with those from the repository. Ensure your backups are safely stored in case you need to revert.

5. Set Fish as Default Shell

This repository uses Fish as the default shell for the terminal. If you're not using Fish already, you can set it as the default shell by running:

chsh -s /usr/bin/fish

After setting Fish as the default shell, close and reopen your terminal to see the changes.

6. Restart Your System

To ensure the changes take effect fully, it's recommended to restart your system or log out and back in:

sudo reboot


---

⚠️ Warnings & Notes

Backup: Always back up your existing configurations before applying new dotfiles. If anything goes wrong, you can always restore from the backup.

Customization: The configuration files are designed to be a starting point. Adjust settings specific to your hardware and preferences, such as monitor setup or input configuration.

Troubleshooting: If you encounter issues, you can check logs in ~/.config/hypr/hyprland.log for error messages.



---

🔧 Customization (Optional)

Adjust configurations for Hyprland, Waybar, Kitty, Neovim, and Fish according to your preferences.


---

❓ Troubleshooting

1. Hyprland won't start: Check the logs in ~/.config/hypr/hyprland.log.


2. Waybar doesn’t show properly: Review and adjust ~/.config/waybar/config.


3. Kitty Terminal shows no icons: Install Nerd Fonts if not already installed:

sudo apt install fonts-nerd-fonts-complete


4. Fish shell not working properly: Ensure Fish is installed and set as the default shell:

chsh -s /usr/bin/fish




---

🔥 Conclusion

Following this guide, you should now have a fully functional, aesthetically pleasing, and efficient Hyprland + Ubuntu 24.04 setup. Enjoy your new environment!


---

Plain Text Version of the Instructions:

1. Install Dependencies

Before installing the dotfiles, ensure that you have all the required dependencies installed. Run the following command to install the necessary packages:

sudo apt update
sudo apt install hyprland waybar kitty neovim fish rofi fonts-nerd-fonts-complete spicetify-cli git

Explanation:

Hyprland: A Wayland compositor that is fast, efficient, and highly customizable.

Waybar: A customizable status bar for Wayland compositors like Hyprland.

Kitty: A fast and feature-rich terminal emulator.

Neovim: A text editor built to improve upon Vim with enhanced features and extensibility.

Fish: A user-friendly interactive shell that offers features like autosuggestions and syntax highlighting.

Rofi: A window switcher and application launcher.

Fonts: Nerd fonts provide patched font icons for use with terminals, status bars, and other tools.

Spicetify: A tool for customizing Spotify.


2. Clone the Repository

Clone the dotfiles repository to your home directory:

git clone https://github.com/Matt-FTW/dotfiles.git ~/dotfiles

Make sure that you have Git installed before running this command. You can install it via:

sudo apt install git

3. Backup Existing Configurations

It's always a good idea to back up your current configuration before making any changes. This allows you to revert to your previous setup if necessary.

mkdir -p ~/.config/backup
cp -r ~/.config/hypr ~/.config/backup/
cp -r ~/.config/waybar ~/.config/backup/
cp -r ~/.config/kitty ~/.config/backup/

4. Apply the Dotfiles

Now that you have the repository cloned and your backups in place, apply the dotfiles to your system:

cp -r ~/dotfiles/.config/* ~/.config/

This will replace existing configuration files with those from the repository. Ensure your backups are safely stored in case you need to revert.

5. Set Fish as Default Shell

This repository uses Fish as the default shell for the terminal. If you're not using Fish already, you can set it as the default shell by running:

chsh -s /usr/bin/fish

After setting Fish as the default shell, close and reopen your terminal to see the changes.

6. Restart Your System

To ensure the changes take effect fully, it's recommended to restart your system or log out and back in:

sudo reboot


---

This version of the file includes everything in both markdown format and plain text, ensuring all information is accessible in both styles for convenience. Let me know if you need further adjustments!

