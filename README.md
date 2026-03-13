# Notes.app Plugin for Claude Code

Full CRUD operations for macOS Notes.app from Claude Code. Create, read, update, and delete notes and folders with natural language.

**[Landing page](https://jondwillis.github.io/notes-app-plugin/)** | **[Issues](https://github.com/jondwillis/notes-app-plugin/issues)**

## Install

```bash
# From Claude Code
/plugin marketplace add jondwillis/notes-app-plugin
/plugin install notes-app@jondwillis

# Or clone directly
git clone https://github.com/jondwillis/notes-app-plugin.git
claude --plugin-dir ./notes-app-plugin
```

## Usage

Just describe what you want:

```
/notes list my notes
/notes create a note called "Meeting Notes" with today's agenda
/notes read "Shopping List"
/notes update "Shopping List" to add milk and eggs
/notes delete "Old Draft"
/notes create a folder called "Work"
/notes show shared notes
/notes show my accounts
/notes show attachments on "Project Plan"
```

## How it works

The plugin gives Claude a library of AppleScript templates. When you describe what you want, Claude picks the right template, fills in your parameters, and executes it via `osascript`. No intermediate server — it talks directly to Notes.app.

Tool access is scoped to `Bash(osascript:*)` only. Claude always confirms before destructive operations.

## Capabilities

| Object | Operations |
|--------|-----------|
| **Notes** | Create, Read, Update, Delete, List, Search |
| **Folders** | Create, Delete, List |
| **Accounts** | List all, Default account |
| **Attachments** | List, Count (read-only) |
| **Filters** | Shared notes, Password-protected notes |

## Limitations

- No pin/unpin, tag, or lock support (not exposed by AppleScript API)
- Attachments are read-only (listing only)
- Password-protected note content cannot be read
- First run requires granting automation permission in System Settings > Privacy & Security > Automation

## Requirements

- macOS with Notes.app
- [Claude Code](https://claude.ai/code)

## License

[MIT](LICENSE)
