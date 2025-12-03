# User Story: Remove Display Edge Spaces

## Title
Remove gaps around display edges

## Description
As a user, I want to utilize the full display area without any gaps or spaces around the edges, so that I can maximize screen real estate and have a clean, borderless interface.

## Current State
- There are visible spaces under the top bar
- There are spaces on the left, right, and bottom edges of the display
- The workspace doesn't utilize the full screen area

## Desired State
- No gaps between windows and screen edges
- Windows should be able to extend to the full screen boundaries
- Clean layout that maximizes available screen space while preserving window borders

## Acceptance Criteria
- [ ] Remove gaps between windows and screen edges on all sides
- [ ] Ensure windows can be maximized to full screen while keeping window borders
- [ ] Maintain proper window snapping behavior
- [ ] Preserve workspace switching functionality
- [ ] Test with different window sizes and positions

## Technical Notes
- Likely involves adjusting `gaps_out` settings in hyprland.conf to 0
- Keep `gaps_in` for spacing between windows
- Preserve window border settings
- Should ensure no conflicts with existing workspace or monitor configurations