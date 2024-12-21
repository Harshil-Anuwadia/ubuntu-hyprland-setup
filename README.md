# Hyprland Ubuntu Dotfiles

This repository contains a collection of dotfiles optimized for a clean, efficient Wayland setup using **Hyprland**, **Waybar**, **Kitty**, **Neovim**, **Fish**, and more, designed for **Ubuntu 24.04**. The goal of these dotfiles is to provide a fully functional, aesthetically pleasing, and efficient environment for users of Ubuntu with **Wayland** compositors.

This guide will walk you through the process of installing and setting up these dotfiles on your system, and help you customize your Ubuntu 24.04 environment to maximize your productivity and user experience.

---

## 🚀 Installation Guide

### Step 1: Install Dependencies

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



---

Step 2: Clone the Repository

Clone the dotfiles repository to your home directory:

git clone https://github.com/Matt-FTW/dotfiles.git ~/dotfiles

Notes:

The dotfiles repository contains configuration files that will be applied to your system.

Make sure that you have Git installed before running this command. You can install it via sudo apt install git if necessary.



---

Step 3: Backup Existing Configurations

It's always a good idea to back up your current configuration before making any changes. This allows you to revert to your previous setup if necessary.

mkdir -p ~/.config/backup
cp -r ~/.config/hypr ~/.config/backup/
cp -r ~/.config/waybar ~/.config/backup/
cp -r ~/.config/kitty ~/.config/backup/

Notes:

This step creates a backup of your Hyprland, Waybar, and Kitty configurations, ensuring that you can restore them later if needed.



---

Step 4: Apply the Dotfiles

Now that you have the repository cloned and your backups in place, you can apply the dotfiles to your system. Run the following command to copy the configuration files from the cloned repository into your ~/.config directory:

cp -r ~/dotfiles/.config/* ~/.config/

Notes:

This will replace existing configuration files with the ones from the repository. Ensure that your backups are safely stored in case you need to revert.

The dotfiles include configurations for Hyprland, Waybar, Kitty, Neovim, and Fish, among others.



---

Step 5: Set Fish as Default Shell

This repository uses Fish as the default shell for the terminal. If you're not using Fish already, you can set it as the default shell by running:

chsh -s /usr/bin/fish

Explanation:

The chsh command changes your default shell. Fish is known for its user-friendly features like autocompletion, syntax highlighting, and suggestions.

After setting Fish as the default shell, close and reopen your terminal to see the changes.



---

Step 6: Restart Your System

After applying the dotfiles and setting up Fish, it's recommended to restart your system or log out and log back in for the changes to fully take effect.

sudo reboot

Notes:

A restart ensures that all environment variables, shell changes, and Wayland compositor configurations are loaded correctly.

This will also apply your Hyprland and Waybar settings, and launch your system with the new configuration.



---

⚠️ Warnings & Notes

Backup: It is crucial to back up any existing configurations before applying new dotfiles. If anything goes wrong, you can always restore from the backup you created earlier.

Customization: The configuration files in this repository are designed to be a general starting point. You may need to adjust settings specific to your hardware and preferences, such as monitor setup or input configuration. For example, you can adjust the Hyprland configuration in ~/.config/hypr/hyprland.conf if needed.

Troubleshooting: If Hyprland does not start or behaves unexpectedly, you can check the logs in the following file:

cat ~/.config/hypr/hyprland.log

The logs can provide helpful error messages and warnings for troubleshooting.

Neovim: This repository includes a basic configuration for Neovim. If you are new to Neovim, make sure to explore the documentation for further customization options. You can modify the ~/.config/nvim/init.vim file to fine-tune your Neovim setup.



---

⚙️ Customization (Optional)

Hyprland: Adjust the Hyprland configuration file located at ~/.config/hypr/hyprland.conf to match your specific monitor layout, input devices, and compositor settings.

Waybar: The Waybar configuration can be found in ~/.config/waybar/config. You can modify the appearance and the modules displayed in the status bar.

Kitty: To adjust Kitty terminal settings, open the ~/.config/kitty/kitty.conf file and make any changes based on your preferences.

Neovim: For Neovim, you can further customize your editor by installing plugins and modifying settings in the init.vim file.



---

❓ Troubleshooting

1. Hyprland won't start:

Check the Hyprland log file located at ~/.config/hypr/hyprland.log for any errors.

Ensure your display server (Wayland) is properly configured.



2. Waybar doesn’t show properly:

Review the Waybar configuration in ~/.config/waybar/config. Some modules may need adjustment to fit your screen resolution or preferences.



3. Kitty Terminal shows no icons:

Make sure you have the Nerd Fonts installed. If not, you can install them by running:

sudo apt install fonts-nerd-fonts-complete



4. Fish shell not working properly:

If the Fish shell is not showing as expected, ensure it is installed and set as the default shell with:

chsh -s /usr/bin/fish





---

🔥 Conclusion

By following this guide, you should now have a fully functional, aesthetically pleasing, and highly efficient Hyprland + Ubuntu 24.04 setup using Matt-FTW's dotfiles. This environment is designed to boost productivity, streamline your workflow, and provide a smooth user experience on Wayland.

Enjoy your new setup! 🎉

This expanded `README.md` file includes all necessary installation steps, customization options, troubleshooting tips, and explanations for each part of the process.

