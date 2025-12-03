## Setup Instruction

This repository contains a reinitialized Hyprland configuration based on the current system setup.

1. Install required packages:
   - Hyprland (Wayland compositor)
   - Alacritty (terminal emulator)
   - Dolphin (file manager)
   - Rofi (application launcher)
   - swaylock (lock screen)
   - ashell (custom script - should be placed in ~/.local/bin/)
   
   Use your distribution's package manager (pacman, apt, dnf, etc.)
   
   Example for Arch Linux:
   ```sh
   sudo pacman -S hyprland alacritty dolphin rofi swaylock
   ```
   
   Example for Ubuntu:
   ```sh
   sudo apt install swaylock
   ```

2. Link configuration files to ~/.config/hypr:
```sh
$ ln -s $PWD/* ~/.config/hypr
```

3. Reload configuration to test:
```sh
$ hyprctl config reload
```

## Lock Screen

- Manual lock: Press `SUPER + L` to lock the screen
- The lock screen uses your system password for authentication
- Uses swaylock with dark background color
- For Ubuntu users: Install with `sudo apt install swaylock`
- For Arch users: Can use hyprlock instead with `sudo pacman -S hyprlock`
