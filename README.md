# Notes.app Plugin for Claude Code

CRUD operations for macOS Notes.app via AppleScript.

## Installation

```bash
claude --plugin-dir /Volumes/Sidecar/notes-app-plugin
```

## Usage

```
/notes list my notes
/notes show my folders
/notes create a note called "Meeting Notes" with today's agenda
/notes read the note called "Shopping List"
/notes update "Shopping List" to add milk and eggs
/notes delete the note "Old Draft"
/notes create a folder called "Work"
/notes show shared notes
/notes show my accounts
/notes show attachments on "Project Plan"
```

## Capabilities

- **Notes**: create, read, update, delete, list, search
- **Folders**: create, delete, list (per account)
- **Accounts**: list all, show default
- **Attachments**: list and count (read-only)
- **Filters**: shared notes, password-protected notes

## Limitations

- No pin/unpin, tag, or lock support (not available via AppleScript API)
- Attachments are read-only (listing only, no creation)
- Password-protected note content cannot be read
- First run requires granting automation permission in System Settings

## Requirements

- macOS with Notes.app
- Claude Code
