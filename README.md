## Setup Instruction

This repository contains a reinitialized Hyprland configuration based on the current system setup.

1. Install required packages:
   - Hyprland (Wayland compositor)
   - Alacritty (terminal emulator)
   - Thunar (file manager)
   - Rofi (application launcher)
   - swaylock (lock screen)
   - gvfs-backends (network storage support)
   - ashell (custom script - should be placed in ~/.local/bin/)
   
   Use your distribution's package manager (pacman, apt, dnf, etc.)
   
   Example for Arch Linux:
   ```sh
   sudo pacman -S hyprland alacritty thunar rofi swaylock gvfs gvfs-smb
   ```
   
   Example for Ubuntu:
   ```sh
   sudo apt install thunar gvfs-backends gvfs-fuse swaylock
   ```

2. Link configuration files to ~/.config/hypr:
```sh
$ ln -s $PWD/* ~/.config/hypr
```

3. Reload configuration to test:
```sh
$ hyprctl config reload
```

## File Explorer (Thunar)

- Launch: Press `SUPER + E` to open Thunar file manager
- Lightweight GTK-based file manager optimized for Hyprland
- Supports network storage integration (SMB, WebDAV, SFTP, FTP)
- Perfect for Synology NAS access

### Synology NAS Integration

Thunar supports multiple protocols for accessing your Synology NAS:

1. **SMB/CIFS** (recommended for local network):
   ```
   smb://synology-ip/share-name
   ```

2. **WebDAV** (good for remote access):
   ```
   davs://synology-ip:5006/share-name
   ```

3. **SFTP** (secure option):
   ```
   sftp://username@synology-ip/path/to/share
   ```

### Setup Instructions

1. Open Thunar with `SUPER + E`
2. Go to File → Connect to Server
3. Enter your Synology URL using one of the protocols above
4. Enter credentials when prompted
5. Bookmark the location for quick access

## Lock Screen

- Manual lock: Press `SUPER + L` to lock the screen
- The lock screen uses your system password for authentication
- Uses swaylock with dark background color
- For Ubuntu users: Install with `sudo apt install swaylock`
- For Arch users: Can use hyprlock instead with `sudo pacman -S hyprlock`
