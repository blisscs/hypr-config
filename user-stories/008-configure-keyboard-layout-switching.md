# User Story: Configure Hyprland Keyboard Layout Switching

**As a** multilingual Hyprland user  
**I want** to configure keyboard layout switching between US English and Thai layouts using native XKB options (Method 1)  
**So that** I can efficiently type in multiple languages without leaving my keyboard workflow

### Acceptance Criteria
- [ ] Configure multiple keyboard layouts (US English and Thai) in Hyprland input settings
- [ ] Set up keyboard layout toggle using Win+Space key combination with native XKB method (Method 1)
- [ ] Add visual notification when keyboard layout changes
- [ ] Ensure layout switching works across all applications and workspaces
- [ ] Verify current layout can be detected and displayed

### Implementation Notes
- **Files to modify**: `hyprland.conf` input section
- **Current state**: `kb_layout = us`, `kb_options = ""` (needs modification)
- **Target configuration**: 
  - `kb_layout = us,th` (add Thai layout)
  - `kb_options = grp:win_space_toggle` (Win+Space toggle)
- **Dependencies**: `jq` for JSON parsing in notification script
- **Keybind pattern**: Use existing `$mainMod` variable (SUPER key)
- **Method selection**: Using Method 1 (native XKB `grp:win_space_toggle`) for better performance and reliability

### Technical Approach
1. **Primary Method**: Use `kb_options = grp:win_space_toggle` for native XKB switching
2. **Notification**: Add keybind to show current layout using `hyprctl notify`
3. **Layout detection**: Use `hyprctl devices -j` with `jq` to get current active keymap

### Testing
- Verify Win+Space toggles between US and Thai layouts
- Test layout switching in different applications (terminal, browser, text editor)
- Check that layout persists when switching workspaces
- Use `hyprctl devices -j | jq '.keyboards[] | .active_keymap'` to verify current layout
- Test notification display when layout changes
- Use `hyprctl reload` to apply configuration changes

### Configuration Validation
- Ensure Thai keyboard layout is available on system (`localectl list-x11-keymap-layouts | grep th`)
- Verify `jq` is installed for JSON parsing
- Test that existing keybinds continue to work after modification

### Implementation Steps
1. Check system Thai layout availability
2. Update `hyprland.conf` input section with multi-layout configuration
3. Add notification keybind for layout changes
4. Test configuration with `hyprctl reload`
5. Verify functionality across applications and workspaces
