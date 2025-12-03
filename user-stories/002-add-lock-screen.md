# User Story: Add Lock Screen

## Title: Add lock screen functionality

**As a** Hyprland user
**I want** a secure lock screen that activates manually and automatically
**So that** I can protect my workstation when away and ensure privacy

### Acceptance Criteria
- [x] Install lock screen package (swaylock for Ubuntu, hyprlock for Arch)
- [x] Create lock screen configuration with proper styling
- [x] Add SUPER + L keybind to manually lock the screen
- [x] Configure lock screen to match current color scheme
- [ ] Test lock/unlock functionality works correctly
- [x] Update README.md with lock screen setup instructions

### Implementation Notes
- Use swaylock for Ubuntu (readily available in repositories)
- Use hyprlock for Arch (official Hyprland lock screen)
- Configure lock screen with dark background matching theme
- Add keybind to hyprland.conf keybinds section
- Use $mainMod variable for consistency with existing keybinds
- Test with `hyprctl config reload` after configuration changes

### Files to Modify
- `hyprland.conf` - Add lock screen keybind
- `README.md` - Update installation and setup instructions
- `hyprlock.conf` - Optional configuration file for Arch users

### Testing
- Press SUPER + L to test manual lock activation
- Verify password field appears and accepts input
- Test unlock functionality with correct password
- Use `hyprctl config reload` to apply configuration changes
- Ensure lock screen integrates properly with Hyprland

---

## Implementation Details

### Package Installation
```bash
# For Ubuntu/Debian:
sudo apt install swaylock

# For Arch Linux:
sudo pacman -S hyprlock

# For Fedora:
sudo dnf install swaylock
```

### Status
✅ **Configuration Complete** - All configuration files have been created and updated.

⚠️ **Package Required** - Install lock screen package to enable functionality:
- Ubuntu: `sudo apt install swaylock`
- Arch: `sudo pacman -S hyprlock`

### Next Steps
1. Install appropriate lock screen package for your distribution
2. Test lock screen by pressing `SUPER + L`
3. Verify unlock functionality with your system password

### Notes
- Ubuntu uses swaylock (more readily available in repositories)
- Arch can use hyprlock (official Hyprland lock screen)
- Both use system password for authentication
- Configuration uses dark background matching theme

### Configuration Structure
- Lock screen keybind: SUPER + L
- Background: Solid color matching current theme
- Input field: Centered with proper styling
- Colors: Match existing Hyprland color scheme