## Setup Instruction

This repository contains a reinitialized Hyprland configuration based on the current system setup.

1. Install required packages:
   - Hyprland (Wayland compositor)
   - Alacritty (terminal emulator)
   - Dolphin (file manager)
   - Rofi (application launcher)
   - ashell (custom script - should be placed in ~/.local/bin/)
   
   Use your distribution's package manager (pacman, apt, dnf, etc.)

2. Link configuration files to ~/.config/hypr:
```sh
$ ln -s $PWD/* ~/.config/hypr
```

3. Reload configuration to test:
```sh
$ hyprctl config reload
```
