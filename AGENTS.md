# AGENTS.md

## Build/Test Commands
This is a Hyprland configuration repository with no build/test commands.
- Install: `ln -s $PWD/* ~/.config/hypr`
- Validate: `hyprctl reload` to test configuration changes

## Code Style Guidelines
- File format: Hyprland configuration syntax (key = value)
- Indentation: 4 spaces for nested blocks
- Comments: Use # for single-line comments
- Variables: Prefix with $ (e.g., $terminal, $mainMod)
- Colors: Use rgba() format with transparency
- Organization: Group related settings in sections with descriptive headers
- Keyboard layout: Include multiple layouts with comma separation (us, th)
- Keybinds: Use $mainMod for SUPER key consistency
- Window rules: Prefer windowrulev2 over windowrule for better specificity