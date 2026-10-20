# Changelog

DiskSpace AI updates itself. Also at [diskspaceai.com/whats-new](https://diskspaceai.com/whats-new).

## 1.0.6

- Help now explains clearly what leaves your Mac: only the license and update checks, and, if you connect a cloud AI agent, the folder names and sizes the app returns to it (never the contents of your files).
- A new guide on the web to connect your agent: diskspaceai.com/mcp.

## 1.0.5

- Connect DiskSpace AI to Claude Code or Claude Desktop with one click from Settings → AI: no Terminal needed. Claude Code picks it up inside the Claude desktop app too.
- “Old Claude Code versions” no longer selects the version a shortcut points to (like ~/.local/bin/claude), so it never breaks it.

## 1.0.4

- Connect DiskSpace AI to your AI agent (Claude Code, Codex, Claude Desktop…) from Settings → AI: the command now comes inside the app.
- Your agent can analyze the disk, see what's in each folder, explain the unknown ones and propose a cleanup.
- It always asks before cleaning, follows the same rules as the app (your protected folders are never touched) and your files are kept for 7 days.
- All release notes, on the web too: diskspaceai.com/whats-new.

## 1.0.3

- When you open a block with the magnifier, each folder shows what it holds inside it: you see two levels at a glance, without clicking.
- Folders that only wrap another one (a “.bundle”, a “data”…) are skipped automatically: Claude's virtual machine goes straight to its disk, rootfs.img.
- Each block's card tells you the biggest items inside.

## 1.0.2

- Look inside any block: hover over it and click the magnifier with “+” (or the same magnifier on its row in the list). The map shows its folders and how much each one takes up, and you can keep going in.
- The path at the top takes you back (or press Esc). Inside, you only look: nothing is selected or deleted.
- In the list, the folder icon opens the Finder and the magnifier opens the block on the map.
- The diskspace command in Terminal now speaks English too (clean, undo, ask…).

## 1.0.1

- The map reads at a glance: selected blocks are solid with a ✓, the ones left out are pale with a border, and the ones that can't be cleaned right now are striped.
- Hover over any block, even the smallest, and a card shows right away what it is, its size and whether it's selected.
- Click a block and the list on the right takes you to its row and highlights it.
- Selected rows in the list are tinted with their color.

## 1.0.0

- This window: after every update it tells you what changed (and it's always in Help → What's New).
- Keyboard shortcuts: ⌘R analyzes, ⌘E explains with AI, ⇧⌘S selects the safe items and ⌘⌫ cleans (always with confirmation).
- New help: where Settings are, the shortcuts, and why a folder takes up less here than in the Finder.
- “Quit the app first” always shows the app's name.


**During the beta**


- Weekly automatic cleanup (Pro) and a notification when space runs low.
- Caches from apps like Slack, Discord, Cursor or VS Code, and a Settings button in the window.
- Accurate figures: files cloned by APFS are counted once.
- Xcode simulators one by one, iCloud Drive, macOS installers and apps you don't use.

## 0.9.9

- A Settings button in the window and in the menu bar panel.
- The menu bar panel shows when the weekly cleanup is due and how much the last one freed.
- Updates now tell you here what has changed.


**In earlier versions**


- Weekly automatic cleanup (Pro) and a notification when space runs low.
- Caches from apps like Slack, Discord, Cursor or VS Code.
- More accurate figures: files cloned by APFS are no longer counted twice.
- Xcode simulators one by one and seven new kinds of folders.
