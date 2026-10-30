# Changelog

DiskSpace AI updates itself. Also at [diskspaceai.com/whats-new](https://diskspaceai.com/whats-new).

## 1.0.21

- New “Send Feedback” window (in the Help menu, in Help and in Settings): tell us an idea or a bug without leaving the app and, if you leave your email, we'll reply.
- If something's wrong, you can attach technical diagnostics: version, macOS, disk space, what the app found and errors from the last cleanup. You see it all before sending, and it never includes file names or paths.

## 1.0.20

- When your disk is almost full, a banner at the top tells you how much is left, gets back the safe items with one button and shows the three biggest things you need to decide on.
- Big items to review now say when you last used or changed them: “changed today”, “unchanged for 6 months”. Simulators that are shut down show their real date instead of “never opened”.
- “Show Whole Disk” splits the gray block into macOS, Applications and your files.
- AI explanations are shown in full and always in the app's language.

## 1.0.19

- While cleaning, a window shows how it's going: what it's cleaning, how many items are left and how much has been freed so far. When it finishes it checks the disk and shows the result in the same window.
- The “All clean!” summary now appears after every cleanup, not just big ones. Confetti is saved for when you pass half a gigabyte.
- If nothing could be cleaned, the app tells you why.

## 1.0.18

- New help: one search box that filters the questions as you type (press Return to ask Apple's AI), “how it works” in three steps and the questions grouped by topic.
- Every answer has a button to do it: show Recently Cleaned, open Photos or the Explorer, connect your AI agent… Plus related questions to keep reading.
- New questions: whether the app is safe and signed by Apple, and how to share what you cleaned. Keyboard shortcuts, in a table.

## 1.0.17

- Recognizes three more folders: Perplexity's cache, Apple's Python cache and the cache of Sparkle's generate_appcast tool.
- For your AI agent: if you ask it to clean the dependencies of a project you changed recently, it can now do it, and the plan tells it how to include them.

## 1.0.16

- After cleaning, a window shows how much you cleaned, how your disk looks now, what took the most space and how much you've cleaned in total with DiskSpace AI, with a milestone when you reach 10, 50 or 100 GB.
- Share it in one click: with the macOS share menu, posting it on X or copying the image to paste anywhere. The card is new and lighter, and it only shows categories: never project names or paths.

## 1.0.15

- Signed and notarized by Apple: it opens without warnings, and macOS checks nobody has modified it.
- Permissions stay: from this version on, updates no longer ask again for access to your folders or Photos. This one asks one last time.

## 1.0.14

- Explorer: a window like Windows Explorer, but with what each folder really takes. A tree on the left, a sortable table with size, percentage, kind and date, and a name filter. Click “Explorer” at the top or press ⇧⌘E.
- “This Mac”: your drives with their free space and what each of your folders takes, at a glance.
- Return opens, ⌫ goes up, space is Quick Look. With right-click, archive or set aside your own things for 7 days, always asking first.

## 1.0.13

- File → “Archive a Folder…” (⇧⌘A): choose any folder or file of yours and see how much you'd save before archiving it.
- “To Archive” is always in the list, with “Choose…” to archive whatever you decide.
- For safety, whole macOS folders, Library, apps and libraries can't be archived.

## 1.0.12

- Archive instead of delete: projects unchanged for months and large forgotten files that compress well show up under “To Archive”, with the savings actually measured.
- “Archive” creates a .zip next to the original (it opens with a double-click on any Mac), checks it fully, and only then sets the original aside for 7 days, with Undo. If anything fails, nothing is touched.
- Also with right-click → “Archive…” on large forgotten files.

## 1.0.11

- Similar photos: nearly identical shots taken in a row, grouped. Apple's AI, on your Mac, suggests keeping the best one in each group.
- Duplicates in Photos: exact copies of the same photo or video. See each group together with the one that stays marked, or merge them with Photos' own tool.
- Duplicate photos and videos in your folders (Pictures, Downloads, Desktop…), even small ones. The one in the most stable place stays.
- Double-click a photo to see it large before deciding.

## 1.0.10

- A “Photos” button at the top, to review the screenshots, large videos and bursts in your library without digging through menus.
- Photos and videos: the app quit when you clicked “Remove”. It works now: macOS asks you to confirm and what you remove goes to “Recently Deleted”.
- Photo thumbnails no longer overlap each other.

## 1.0.9

- Photos and videos: review the screenshots, videos over 100 MB and extra burst photos in your library. Nothing is preselected, and what you remove goes to Photos' “Recently Deleted” (30 days). Open it from the “Photos library” row or Edit → Review Photos and Videos…
- Other drive: see what's taking space on an external drive on the map, with the magnifier, search and Quick Look. View only.
- Desktop screenshots: they show up together so you can review them; the ones you clean are kept 7 days.

## 1.0.8

- Installers already used: the .dmg of an app you already have installed, or a .zip you already extracted, now show as safe to delete. What they contained is already on your Mac.
- Quick Look: press the space bar over a block on the map or a row to see what it is without opening anything, like in the Finder. It's also in the right-click menu.
- Search: type above the list (or press ⌘F) to see only what matches; the rest dims on the map.
- Pro includes free updates.

## 1.0.7

- Licenses are ready: when you buy Pro, paste the key from the email and click Activate. It works on up to 3 Macs and you can move it from one to another.
- Lost your key? A link next to the box takes you to your orders, where you get it back with your email.
- End-of-beta notice: in December you'll see how many days are left, and on January 1 the app explains what stays free. Nothing stops working suddenly or without warning.
- If the weekly cleanup pauses because you don't have Pro, the menu bar panel says so.

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
