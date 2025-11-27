# Claude Code Interactive Mode

Quick reference for keyboard shortcuts and commands in Claude Code's interactive REPL.

## Keyboard Shortcuts

### General Controls

| Shortcut | Action |
|----------|--------|
| Ctrl+C | Cancel current input or generation |
| Ctrl+D | Exit session |
| Ctrl+L | Clear screen (preserves conversation history) |
| Ctrl+O | Toggle verbose output (show tool details) |
| Ctrl+R | Search command history (reverse search) |
| Up/Down | Navigate previous inputs |
| Tab | Toggle extended thinking mode |
| Shift+Tab | Switch permission modes |
| Alt+M | Switch permission modes (alternate) |
| Esc Esc | Restore conversation/code to previous checkpoint |

### Clipboard

| Shortcut | Action |
|----------|--------|
| Ctrl+V | Paste image from clipboard (macOS/Linux) |
| Alt+V | Paste image from clipboard (Windows) |

### Background Tasks

| Shortcut | Action |
|----------|--------|
| Ctrl+B | Move current bash command to background |
| Ctrl+B Ctrl+B | Background command in Tmux (press twice) |

## Multiline Input

| Method | Action |
|--------|--------|
| \ + Enter | Escape newline for continuation |
| Option+Enter | macOS default multiline |
| Shift+Enter | After running `/terminal-setup` |
| Ctrl+J | Insert line feed character |
| Paste | Pastes multi-line content directly |

## Input Prefixes

| Prefix | Action |
|--------|--------|
| # | Add text to CLAUDE.md memory |
| / | Execute slash command |
| ! | Run bash command directly (output added to context) |
| @ | File path autocomplete |

## Slash Commands

### Session & Navigation

| Command | Action |
|---------|--------|
| /help | Show help information |
| /clear | Clear conversation history |
| /compact | Compact conversation with optional focus instructions |
| /context | Visualize current context usage as colored grid |
| /cost | Show token usage and cost |
| /usage | Display plan usage limits and rate info |
| /resume | Resume a previous conversation |
| /rewind | Rewind conversation and/or code to earlier state |
| /exit | Exit the REPL |

### Configuration

| Command | Action |
|---------|--------|
| /config | Open Settings interface (Config tab) |
| /status | Open Settings interface (Status tab) |
| /statusline | Configure status line UI |
| /model | Select or change the AI model |
| /output-style | Set output style (text, json, etc.) |
| /permissions | Manage access controls |
| /privacy-settings | View and update privacy settings |
| /terminal-setup | Install keyboard bindings for multiline input |
| /vim | Enable vim editing mode |

### Project & Memory

| Command | Action |
|---------|--------|
| /init | Initialize project with CLAUDE.md guide |
| /memory | Edit CLAUDE.md memory files |
| /add-dir | Add additional working directories |
| /todos | List current todo items |

### Tools & Integrations

| Command | Action |
|---------|--------|
| /agents | Manage custom AI subagents |
| /bashes | List and manage background tasks |
| /hooks | Manage hook configurations for tool events |
| /ide | Show IDE integration status |
| /mcp | Manage MCP server connections |
| /plugin | Manage Claude Code plugins |
| /sandbox | Enable isolated execution environment |

### Review & Debugging

| Command | Action |
|---------|--------|
| /review | Request code review |
| /security-review | Conduct security assessment of changes |
| /pr-comments | View pull request comments |
| /doctor | Check Claude Code installation health |
| /bug | Report bugs (sends conversation to Anthropic) |
| /release-notes | View release notes |

### Account

| Command | Action |
|---------|--------|
| /login | Switch Anthropic accounts |
| /logout | Sign out from Anthropic account |
| /install-github-app | Configure Claude GitHub Actions |
| /export | Export conversation to file or clipboard |

## Vim Mode

Enable with `/vim` command or set permanently via `/config`.

### Mode Switching

| Key | Action |
|-----|--------|
| Esc | Enter NORMAL mode |
| i | Insert before cursor |
| I | Insert at line beginning |
| a | Insert after cursor |
| A | Insert at line end |
| o | Open line below |
| O | Open line above |

### Navigation (NORMAL mode)

| Key | Action |
|-----|--------|
| h/j/k/l | Left/down/up/right |
| w | Next word start |
| e | Next word end |
| b | Previous word start |
| 0 | Line beginning |
| $ | Line end |
| gg | Document start |
| G | Document end |

### Editing (NORMAL mode)

| Key | Action |
|-----|--------|
| x | Delete character |
| dd | Delete line |
| D | Delete to end of line |
| dw | Delete word forward |
| db | Delete word backward |
| cc | Change entire line |
| C | Change to end of line |
| cw | Change word forward |
| . | Repeat last command |

## Permission Modes

Toggle with Shift+Tab or Alt+M:

- **Normal** - Prompts for each tool use
- **Auto-Accept** - Automatically approves tool calls
- **Plan** - Research/planning mode without code changes

## CLI Usage

| Command | Action |
|---------|--------|
| `claude` | Start interactive REPL |
| `claude "query"` | Start REPL with initial prompt |
| `claude -p "query"` | Run query non-interactively, then exit |
| `cat file \| claude -p "query"` | Process piped content |
| `claude -c` | Continue most recent conversation |
| `claude -r <session-id>` | Resume specific session by ID |
| `claude update` | Update to latest version |
| `claude mcp` | Configure MCP servers |

### Common CLI Flags

| Flag | Action |
|------|--------|
| `-p, --print` | Print response without interactive mode |
| `-c, --continue` | Continue most recent conversation |
| `-r, --resume <id>` | Resume session by ID |
| `--model <name>` | Set model (sonnet, opus, or full name) |
| `--output-format` | Output format: text, json, stream-json |
| `--system-prompt` | Replace system prompt with custom text |
| `--append-system-prompt` | Append to default system prompt |
| `--add-dir <path>` | Add additional working directory |
| `--max-turns <n>` | Limit agentic turns |
| `--permission-mode` | Start in specified permission mode |
| `--allowedTools` | Tools permitted without prompts |
| `--disallowedTools` | Tools blocked without prompts |
| `--verbose` | Enable verbose logging |

## Custom Slash Commands

Create custom commands as Markdown files:
- Personal: `~/.claude/commands/`
- Project: `.claude/commands/`

## Notes

- Extended thinking (Tab) uses more tokens but improves complex reasoning
- Background tasks run asynchronously with task IDs for tracking
- Checkpoints (Esc Esc) allow reverting code and conversation state
- Memory prefix (#) persists information across sessions in CLAUDE.md
- Custom commands support arguments, bash execution, and file references
