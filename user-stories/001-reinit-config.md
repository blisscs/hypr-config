# User Story: Reinitialize Configuration Files

## Title: Reinitialize Hyprland configuration files

**As a** Hyprland user
**I want** to remove and regenerate the current hyprland.conf and hyprlock.conf files
**So that** I can start with a clean, fresh configuration setup

### Acceptance Criteria
- [ ] Remove existing hyprland.conf file
- [ ] Remove existing hyprlock.conf file
- [ ] Copy ~/.config/hypr/hyprland.conf to repository as new base
- [ ] Update README.md to reflect the reinitialized configuration
- [ ] Verify both files are properly set up in the repository

### Implementation Notes
- Use `rm` command to delete both configuration files
- Copy system's current hyprland.conf as the new base configuration
- Update README.md setup instructions to match current state
- Files are located in the root of the repository

### Testing
- Verify new hyprland.conf exists and is readable
- Check git status to confirm file changes
- Validate README.md content is accurate
- Test configuration with `hyprctl config reload`

---

## Execution Commands
```bash
# Remove current files
rm hyprland.conf hyprlock.conf

# Copy system config as base
cp ~/.config/hypr/hyprland.conf .

# Update README.md (manual edit required)
# Update setup instructions to reflect current state

# Verify changes
ls -la | grep hyprland
git status
```