# DiskSpace AI for your AI agent (MCP server)

DiskSpace AI comes with an [MCP](https://modelcontextprotocol.io) server: your agent (Claude Code, Claude Desktop, Codex, Cursor…) can analyze your Mac's disk, see what's in each folder, explain the unknown ones and propose a safe cleanup. It always asks before cleaning.

> “Free up 20 GB for me, I need to update macOS.”
>
> I can free **21.4 GB with no risk**: 9.4 GB of Xcode build data, 6.8 GB of uv cache and 5.2 GB of node_modules from idle projects. I won't touch your Docker or your photos. Shall I?

## Connect with one click

1. [Download DiskSpace AI](https://diskspaceai.com/download) (1.0.5 or later) and open it.
2. Open **Settings → AI → Connect your AI agent** and click **Connect** for Claude Code or Claude Desktop. No Terminal needed; Claude Code also works inside the Claude desktop app.
3. Start a new session and ask “what's taking up space on my Mac?”.

## Claude Desktop only, without the app

Download `diskspace-ai-<version>.mcpb` from the [latest release](https://github.com/diskspaceai/diskspace-ai/releases/latest) and double-click it: Claude Desktop installs it as an extension. It's the same server, signed and notarized by Apple.

## Other agents

The server is the `diskspace` command inside the app, with the `mcp` argument (stdio).

**Claude Code** (Terminal):

```bash
claude mcp add diskspace-ai -- "/Applications/DiskSpace AI.app/Contents/MacOS/diskspace" mcp
```

**Codex:**

```bash
codex mcp add diskspace-ai -- "/Applications/DiskSpace AI.app/Contents/MacOS/diskspace" mcp
```

**Cursor, Windsurf and any other with a JSON config:**

```json
{
  "mcpServers": {
    "diskspace-ai": {
      "command": "/Applications/DiskSpace AI.app/Contents/MacOS/diskspace",
      "args": [
        "mcp"
      ]
    }
  }
}
```

## Tools

| Tool | What it does | |
|---|---|---|
| `analyze_disk` | Free space and every known folder with its size, what it is, whether it's safe to delete (safe / review / keep) and how to clean it. Also project dependencies and unclassified folders. | Read-only |
| `folder_contents` | What's inside a folder, two levels deep, with real sizes; skips folders that only wrap another one. | Read-only |
| `explain_folder` | Explains an unknown folder with Apple's AI, on the Mac. It never marks it as safe. | Read-only |
| `plan_cleanup` | Dry run: what would be cleaned and why the rest is skipped. | Read-only |
| `clean` | Cleans the chosen items. Requires `confirm: true`. | Asks first |
| `undo_last_cleanup` | Restores what the last cleanup set aside. | Undo |

## Guarantees

- **It never cleans without your OK**: `clean` requires explicit confirmation and the server tells the agent to show you the plan first.
- **Your files are kept 7 days**: only what recreates itself is deleted right away; everything else can be undone.
- **The same rules as the app**: folders you protected in Settings are never touched, nor anything from open apps.
- **Analyzing is free; cleaning is Pro** (free during the beta).

## Privacy

The server runs entirely on your Mac and only talks to the agent you have open. If your agent uses a cloud model, that service sees what DiskSpace AI returns to it (folder names, paths and sizes, never the contents of your files), under its own privacy policy.

## Try asking

- “What's taking up space on my Mac?”
- “Free up 20 GB without touching my files.”
- “What's inside my Xcode simulators?”
- “Clean the developer caches and show me the plan first.”

More: [diskspaceai.com/mcp](https://diskspaceai.com/mcp)
