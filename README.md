## 🥳 Setup

<img src="https://i.imgur.com/C4FpPiG.png">

#### Installing needed dependencies 📦
	
```sh
paru -S hyprland-git polkit-kde-agent dunst grimblast rofi rofi-emoji wl-clipboard wf-recorder wlogout grimblast-git hyprpicker-git xdg-desktop-portal-hyprland-git ffmpegthumbnailer tumbler wtype imagemagick swaylock-effects qt5-wayland qt6-wayland ripgrep waybar-hyprland-git
```

**Extras*
```sh
# themes
paru -S catppuccin-gtk-theme-mocha catppuccin-cursors-mocha catppuccin-mocha-grub-theme-git nwg-look
# apps
paru -S ranger zsh neovim noise-suppression-for-voice
```

**If you want a Graphical file-manager*
```sh
thunar thunar-archive-plugin file-roller   
```

**Fonst*
```sh
paru -S nerd-fonts-jetbrains-mono ttf-material-design-icons
```

**Prompt*
```sh
sh -c "$(curl -fsSL https://gitee.com/mirrors/oh-my-zsh/raw/master/tools/install.sh)"
```

#### Installing dotfiles 🚀
```sh
git clone https://github.com/k1tyoo/hyprland-dots.git && cd hyprland-dots
cp -r .local/bin ~/ && chmod -r 755 ~/.local/bin
echo 'export PATH="$HOME/.local/bin:PATH" >> ~/.zshrc
cp -r .config ~/
cp -r .wallpapers ~/
```

**launch Hyprland with wrappedhl*

Note the environment variables configured before use
```sh
cd /usr/share/wayland-sessions
sudo mv hyprland.desktop wrapped_hl.desktop

# change Exec to the absolute path of wrappedhl
# Exec=/home/username/.local/bin/wrappedhl
```

## Credits

_Beauty community: [r/unixporn](https://www.reddit.com/r/unixporn)._

_Awesome waybar setup: © [Ruixi-rebirth](https://github.com/Ruixi-rebirth)_

_The most user-friendly neovim configuration: © [ayamir](https://github.com/ayamir)_ 🤯

