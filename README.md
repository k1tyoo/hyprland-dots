# Overview

- **Window Manager** • [Hyprland](https://github.com/hyprwm/Hyprland)
- **Terminal** • [Kitty](https://sw.kovidgoyal.net/kitty/)
- **Shell** • [Zsh](https://www.zsh.org)
- **Prompt** • [Oh-my-zsh](https://ohmyz.sh/)
- **Panel** • [Waybar](https://aur.archlinux.org/packages/waybar-hyprland-git)
- **Notify Daemon** • [Dunst](https://github.com/dunst-project/dunst)
- **Launcher** • [Rofi](https://github.com/davatorium/rofi)
- **File Manager** • [Ranger](https://github.com/ranger/ranger)

---

<img src="https://i.imgur.com/C4FpPiG.png">

---

## 🥳 Setup

#### Installing needed dependencies 📦

```sh
yay -S hyprland-git polkit-kde-agent wl-clipboard wf-recorder wlogout grimblast-git hyprpicker-git xdg-desktop-portal-hyprland-git ffmpegthumbnailer tumbler wtype imagemagick swaylock-effects swayidle qt5-wayland qt6-wayland waybar-hyprland-git swww-git network-manager-applet blueman python-pip
```

_Make things rust_

```sh
yay -S fd bat exa ripgrep ripgrep-all dust procs btop nvtop
```

#### Extra 👽

_Theme_

```sh
yay -S catppuccin-gtk-theme-mocha catppuccin-cursors-mocha catppuccin-mocha-grub-theme-git nwg-look
```

_App_

```sh
yay -S rofi rofi-emoji dunst ranger zsh neovim kitty
```

_Graphical file-manager_

```sh
yay -S thunar thunar-archive-plugin file-roller
```

_Fonts_

```sh
yay -S ttf-jetbrains-mono-nerd ttf-material-design-icons
```

_Prompt_

```sh
# zsh
yay -S zsh
chsh -s /bin/zsh
# oy-my-zsh
sh -c "$(curl -fsSL https://gitee.com/mirrors/oh-my-zsh/raw/master/tools/install.sh)"
```

#### Installing dotfiles 🚀

```sh
git clone https://github.com/k1tyoo/hyprland-dots.git && cd hyprland-dots
cp -r .config ~/
```

_launch Hyprland with [wrappedhl](https://wiki.hyprland.org/Getting-Started/Quick-start/)_

Note the environment variables configured before use it

```sh
# wrappedhl
cp -r ~/Downloads/hyprland-dots/.local/bin ~/ && chmod -R 755 ~/.local/bin
echo 'export PATH=$HOME/.local/bin:$PATH' >> ~/.zshrc
# session
cd /usr/share/wayland-sessions/
sudo mv hyprland.desktop wrappedhl.desktop
```

Change session Exec parameter to the absolute path of wrappedhl

#### Personal preference 💻

```sh
yay -S sddm-git spotify octopi firefox font-manager dconf-editor visual-studio-code-bin ntfs-3g
```

_fcitx5_

```sh
yay -S fcitx5-im fcitx5-chinese-addons fcitx5-rime rime-cloverpinyin

# one more thing
mkdir -p ~/.local/share/fcitx5/rime
nvim ~/.local/share/fcitx5/rime/default.custom.yaml
```

_Add the following to the file_

```sh
patch:
  "menu/page_size": 8
  schema_list:
    - schema: clover
```

## Credits

_Beauty community: [r/unixporn](https://www.reddit.com/r/unixporn)._

_Awesome waybar setup: © [Ruixi-rebirth](https://github.com/Ruixi-rebirth)_

_The most user-friendly neovim configuration: © [ayamir](https://github.com/ayamir)_ 🤯
