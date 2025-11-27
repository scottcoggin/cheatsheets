# Terminal Keyboard Shortcuts

Reference for Zsh/Bash terminal shortcuts (works in COSMIC Terminal, VS Code integrated terminal, etc.)

## Line Editing

### Clear/Delete

| Shortcut | Action |
|----------|--------|
| Ctrl+U | Clear from cursor to beginning of line |
| Ctrl+K | Clear from cursor to end of line |
| Ctrl+C | Cancel/clear entire line (new prompt) |
| Ctrl+W | Delete word before cursor |
| Alt+Backspace | Delete word before cursor |
| Ctrl+D | Delete character under cursor (or exit if empty) |
| Backspace | Delete character before cursor |

### Cursor Movement

| Shortcut | Action |
|----------|--------|
| Ctrl+A | Move to beginning of line |
| Ctrl+E | Move to end of line |
| Alt+F | Move forward one word |
| Alt+B | Move backward one word |
| Ctrl+F | Move forward one character |
| Ctrl+B | Move backward one character |

### Undo/Paste

| Shortcut | Action |
|----------|--------|
| Ctrl+Y | Paste last deleted text (yank) |
| Ctrl+_ | Undo last edit |
| Alt+. | Insert last argument of previous command |

## History

| Shortcut | Action |
|----------|--------|
| Ctrl+R | Reverse search history (fuzzy with fzf) |
| Ctrl+P | Previous command (same as Up arrow) |
| Ctrl+N | Next command (same as Down arrow) |
| Alt+. | Insert last argument of previous command |
| !! | Repeat last command |
| !$ | Last argument of previous command |
| !* | All arguments of previous command |

## Screen Control

| Shortcut | Action |
|----------|--------|
| Ctrl+L | Clear screen (keeps current input) |
| Ctrl+S | Pause output (freeze screen) |
| Ctrl+Q | Resume output (unfreeze screen) |

## Job Control

| Shortcut | Action |
|----------|--------|
| Ctrl+Z | Suspend current process (background) |
| Ctrl+C | Interrupt/kill current process |
| fg | Resume suspended job in foreground |
| bg | Resume suspended job in background |
| jobs | List background jobs |

## Zsh-Specific

| Shortcut | Action |
|----------|--------|
| Tab | Autocomplete (with menu selection) |
| Tab Tab | Show all completions |
| Ctrl+T | fzf file search (if configured) |
| Alt+C | fzf directory navigation (if configured) |

## Notes

- These are readline/zle shortcuts that work in most Unix terminals
- Alt key may need to be configured as Meta key in some terminals
- On macOS, use Option key for Alt shortcuts
