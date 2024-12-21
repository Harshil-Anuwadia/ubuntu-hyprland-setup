# 🚀 The Ultimate Guide to Installing Hyprland on Ubuntu!

<div align="center">

![Hyprland in action would go here!]

### 🎮 Transform your Ubuntu into a Ricing Masterpiece! 
*A friendly guide for Ubuntu users diving into the world of Hyprland*

</div>

## 🤔 What's This All About?

Hey Ubuntu friend! 👋 Want to make your desktop look absolutely amazing? You've stumbled upon a guide that'll help you install and set up these awesome Hyprland dotfiles on your Ubuntu 24.04 system! 

> 🎨 *Spoiler alert: Your desktop is about to look incredible!*

## ✨ What You'll Get

After following this guide, your Ubuntu will be blessed with:
- 🖥️ A super sleek Hyprland Wayland compositor
- 🎯 A gorgeous Waybar status bar
- 🐱 The snazzy Kitty terminal
- 📝 A pre-configured Neovim setup
- 🐠 The friendly Fish shell
- 🚀 And much more awesomeness!

## 🎯 Before We Begin

### System Requirements
- 🐧 Ubuntu 24.04 (Trust me, it matters!)
- 🧠 A few brain cells (don't worry, we'll help you preserve them)
- ☕ Maybe a coffee (this is gonna be fun!)

## 🛠️ Let's Get Started!

### Step 1: Install the Goodies 🎁

First, let's get all the cool stuff we need! Copy this magical command:

```bash
sudo apt update && sudo apt install hyprland waybar kitty neovim fish rofi fonts-nerd-fonts-complete spicetify-cli git
```

What's in the goodie bag? 🎒
- 🌈 **Hyprland**: Your window manager (but cooler)
- 📊 **Waybar**: Makes your top bar look awesome
- 🐱 **Kitty**: The cutest terminal ever
- 📝 **Neovim**: Text editor with superpowers
- 🐠 **Fish**: A shell that actually makes sense
- 🎯 **Rofi**: App launcher that sparks joy
- 🎨 **Nerd Fonts**: Because normal fonts are boring
- 🎵 **Spicetify**: Make Spotify match your rice!

### Step 2: Backup Your Stuff! 🎒

Before we dive in, let's make sure your current setup is safe and sound:

```bash
mkdir -p ~/.config/backup
cp -r ~/.config/{hypr,waybar,kitty} ~/.config/backup/
```

> 💡 *Better safe than sorry! Your future self will thank you!*

### Step 3: Get Those Dotfiles! 📦

Time to grab the good stuff:

```bash
git clone https://github.com/Matt-FTW/dotfiles.git ~/dotfiles
cp -r ~/dotfiles/.config/* ~/.config/
```

### Step 4: Make Fish Your Friend 🐠

Let's switch to the friendliest shell in the sea:

```bash
chsh -s /usr/bin/fish
```

> 🎣 *Fish: The shell that makes you smile!*

### Step 5: The Grand Finale 🎉

```bash
sudo reboot
```

> 🔄 *Time for a quick restart - go grab a snack!*

## 🎨 Making It Yours

Want to tweak things? Here's where the magic happens:
- 🖥️ Hyprland: `~/.config/hypr/hyprland.conf`
- 📊 Waybar: `~/.config/waybar/config`
- 🐱 Kitty: `~/.config/kitty/kitty.conf`
- 📝 Neovim: `~/.config/nvim/init.vim`

## 🆘 Help! Something's Not Right!

### Common Oopsies and Fixes:

1. **🤔 Hyprland's Playing Hide and Seek**
   ```bash
   cat ~/.config/hypr/hyprland.log
   ```

2. **📊 Waybar Looks Weird**
   - Check your config at `~/.config/waybar/config`
   - Try turning it off and on again (it works more often than you'd think!)

3. **😿 Kitty's Missing Icons**
   ```bash
   sudo apt install fonts-nerd-fonts-complete
   ```

4. **🐠 Fish Acting Fishy**
   ```bash
   chsh -s /usr/bin/fish
   ```

## 🌟 Credits Where Credits Are Due

Huge thanks to:
- 🙌 The original dotfiles creator for sharing their awesome work
- 🐧 The Ubuntu community for being awesome
- 🎨 The ricing community for the inspiration
- 👩‍💻 You, for giving this a try!

## 🎉 You Made It!

Congratulations! Your Ubuntu is now cooler than ever! Time to show off in r/unixporn! 🎨

> 🎵 *Now playing: "I'm Too Sexy For My Desktop"*

---

<div align="center">

### 🤗 Need Help?

Don't be shy! If something's not working, check out the original dotfiles repository or the Ubuntu community. We've all been there!

*Remember: Every rice master was once a newbie!* 

</div>