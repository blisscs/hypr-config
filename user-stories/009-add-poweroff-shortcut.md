# User Story: Add Poweroff Shortcut

## Title: Add poweroff shortcut

**As a** Hyprland user  
**I want** a keyboard shortcut to power off the computer  
**So that** I can quickly shut down the system  

### Acceptance Criteria
- [ ] SUPER + SHIFT + Q powers off the computer
- [ ] Shortcut works from any workspace

### Implementation Notes
- Modify keybinds section in hyprland.conf
- Use exec command to run systemctl poweroff
- Follow existing keybind pattern

### Testing
- Test the shortcut powers off the system
- Use `hyprctl reload` to apply changes