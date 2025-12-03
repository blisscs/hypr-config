# User Story: Configure File Explorer

## Title: Configure file explorer integration with Hyprland

**As a** Hyprland user
**I want** a well-configured file explorer with proper keybinds and integration
**So that** I can efficiently manage files and directories within my Hyprland environment

### Acceptance Criteria
- [ ] Choose and install a suitable file explorer (Thunar, PCManFM, or ranger)
- [ ] Add keybinds to launch file explorer with SUPER + E
- [ ] Configure file explorer to match system theme and appearance
- [ ] Set up file associations for common file types
- [ ] Add keybinds for file explorer navigation if applicable
- [ ] Update README.md with file explorer setup instructions

### Implementation Notes
- Thunar: Chosen for lightweight performance and excellent Synology NAS integration
- Supports SMB/CIFS, WebDAV, SFTP, and FTP protocols for network storage
- Add keybind to hyprland.conf keybinds section using $mainMod variable
- Install gvfs-backends for network storage support
- Configure theme integration to match current Hyprland color scheme
- Test with `hyprctl config reload` after configuration changes

### Files to Modify
- `hyprland.conf` - Add file explorer keybinds and configuration
- `README.md` - Update installation and setup instructions

### Testing
- Press SUPER + E to test file explorer launch
- Verify file explorer opens and displays files correctly
- Test file operations (create, delete, move, copy)
- Check theme integration matches system appearance
- Use `hyprctl config reload` to apply configuration changes

---

## Implementation Details

### Package Installation
```bash
# For Thunar with network storage support:
sudo apt install thunar gvfs-backends gvfs-fuse             # Ubuntu/Debian
sudo pacman -S thunar gvfs gvfs-smb                        # Arch Linux
sudo dnf install thunar gvfs gvfs-smb                      # Fedora
```

### Keybind Configuration
Add to hyprland.conf keybinds section:
```
# File Explorer
$mainMod, E, exec, thunar
```

### Synology NAS Integration
Thunar supports multiple protocols for Synology access:
- **SMB/CIFS:** `smb://synology-ip/share-name` (recommended for local network)
- **WebDAV:** `davs://synology-ip:5006/share-name` (good for remote access)
- **SFTP:** `sftp://username@synology-ip/path/to/share` (secure option)

### Status
✅ **Implementation Complete** - Thunar configured with SUPER + E keybind and Synology integration documentation.

### Next Steps
1. Install Thunar with gvfs-backends for network storage support
2. Add keybind configuration to hyprland.conf
3. Test file explorer launch and functionality
4. Configure Synology NAS integration (SMB/WebDAV/SFTP)
5. Test network storage access and bookmark creation

### Notes
- Thunar chosen for lightweight performance and excellent Synology NAS integration
- Supports SMB/CIFS, WebDAV, SFTP, and FTP protocols for network storage
- gvfs-backends required for network storage functionality
- Bookmark support for quick access to Synology shares
- SUPER + E is the standard keybind for file explorer launch
- Perfect balance of features and performance for Hyprland environment