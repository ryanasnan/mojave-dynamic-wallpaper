# Note

Please visit original repo in https://github.com/caglarturali/catalina-dynamic-wallpaper for detail information

this repo just for mojave dynamic wallpaper

## Mojave Dynamic Wallpaper

Simple, time-based, macOS style dynamic wallpaper that transitions between the dark and light versions of macOS Catalina's default wallpapers. It also sets the lock screen background to the same image as the desktop background for a consistent look. Designed to be used with [KDEasyMc](https://github.com/caglarturali/KDEasyMc).

### Concept

Explain code

```bash
BIN_DIR="${HOME}/.local/bin"
THEMES_DIR="${HOME}/.local/share/wallpapers"
AUTOSTART_DIR="${HOME}/.config/autostart"
AUTOSTART_SCRIPTS_DIR="${HOME}/.config/autostart-scripts"
```

`BIN_DIR` is for the command (local binary command)

`THEMES_DIR` is for wallpaper set

`AUTOSTART_DIR` is for desktop file (exec on directory `AUTOSTART_SCRIPTS_DIR`) if you are using `DDE`

`AUTOSTART_SCRIPTS_DIR` is for symlink script from `BIN_DIR`

if you uninstall (using command `catalina -u`) all of files under directory above will be deleted

and dont forget to restart your pc (autostart script is still running even the file is deleted)

### Screenshot

![](screenshots/screenshot.gif)

### Installation

- Clone the repo.

  ```bash
  git clone https://github.com/ryanasnan/mojave-dynamic-wallpaper
  cd mojave-dynamic-wallpaper
  ```

- Install.
  - `./install --kde` or `-k` on KDE Plasma 5
  - `./install --dde` or `-d` on DDE

### Usage

You can control the wallpaper through control script.

`~/.local/bin/catalina` **[OPTIONS...]** or `catalina` **[OPTIONS...]**

| OPTIONS:        |                                                         |
| :-------------- | :------------------------------------------------------ |
| -s, --start     | Start dynamic wallpaper.                                |
| -p, --stop      | Stop dynamic wallpaper.                                 |
| -u, --uninstall | Uninstall dynamic wallpaper. Removes all related files. |
| -h, --help      | Show this help.                                         |

### Notes

- On DDE, it only sets the desktop background. You need to set the lock screen background manually, for now.

### Credits :blush:

- https://github.com/caglarturali/catalina-dynamic-wallpaper.git
- [macOS Catalina](https://www.apple.com/macos/catalina-preview/)
- [@RaitaroH](https://gitlab.com/RaitaroH) from GitLab. This project is heavily inspired by his [dynamic-wall](https://gitlab.com/RaitaroH/dynamic-wall) and [KDE-Terminal-Wallpaper-Changer](https://gitlab.com/RaitaroH/KDE-Terminal-Wallpaper-Changer) repos.
