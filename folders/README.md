# What every folder on your Mac is, and whether you can delete it

The 70 folders and caches DiskSpace AI knows. **Recreates itself**: the tool that made it creates it again. **Review**: it may hold something of yours. **Your data**: don't delete it. Each one has its own page in the [web guide](https://diskspaceai.com/folders).

Also as [JSON](folders.json), to use in your scripts. Missing one? [Open an issue](../../../issues/new/choose).

## Package caches

| Folder | Where | Verdict | How to free it |
|---|---|---|---|
| [uv cache (Python)](https://diskspaceai.com/folders/uv-cache)<br><sub>Python packages uv already downloaded. It fetches them again when needed.</sub> | `~/.cache/uv` | 🟢 Recreates itself | With the tool's own command: `uv cache clean` |
| [pip cache](https://diskspaceai.com/folders/pip-cache)<br><sub>Python packages downloaded by pip.</sub> | `~/Library/Caches/pip` | 🟢 Recreates itself | With the tool's own command: `pip cache purge` |
| [npm cache](https://diskspaceai.com/folders/npm-cache)<br><sub>Copies of packages npm already installed. It downloads them again if needed.</sub> | `~/.npm/_cacache` | 🟢 Recreates itself | With the tool's own command: `npm cache clean --force` |
| [npx temporary packages](https://diskspaceai.com/folders/npx-cache)<br><sub>Tools npx downloaded to run once.</sub> | `~/.npm/_npx` | 🟢 Recreates itself | By emptying the folder's contents (the folder stays). |
| [pnpm store](https://diskspaceai.com/folders/pnpm-store)<br><sub>Packages shared by your projects. “prune” only removes the ones no project uses.</sub> | `~/Library/pnpm/store` | 🟢 Recreates itself | With the tool's own command: `pnpm store prune` |
| [pnpm cache](https://diskspaceai.com/folders/pnpm-cache)<br><sub>Package metadata downloaded by pnpm.</sub> | `~/Library/Caches/pnpm` | 🟢 Recreates itself | By emptying the folder's contents (the folder stays). |
| [Yarn cache](https://diskspaceai.com/folders/yarn-cache)<br><sub>Packages downloaded by Yarn.</sub> | `~/Library/Caches/Yarn` | 🟢 Recreates itself | With the tool's own command: `yarn cache clean` |
| [Bun cache](https://diskspaceai.com/folders/bun-cache)<br><sub>Packages downloaded by Bun.</sub> | `~/.bun/install/cache` | 🟢 Recreates itself | With the tool's own command: `bun pm cache rm` |
| [Homebrew cache](https://diskspaceai.com/folders/homebrew-cache)<br><sub>Installers for programs Homebrew already installed.</sub> | `~/Library/Caches/Homebrew` | 🟢 Recreates itself | With the tool's own command: `brew cleanup -s` |
| [Gradle cache](https://diskspaceai.com/folders/gradle-cache)<br><sub>Dependencies for Android and Java projects. The next build will take longer.</sub> | `~/.gradle/caches` | 🟢 Recreates itself | By emptying the folder's contents (the folder stays). |
| [Downloaded Gradle versions](https://diskspaceai.com/folders/gradle-wrapper)<br><sub>Each project downloads the Gradle version it asks for. Downloaded again when you build.</sub> | `~/.gradle/wrapper/dists` | 🟢 Recreates itself | By emptying the folder's contents (the folder stays). |
| [Temporary Rust for Python packages](https://diskspaceai.com/folders/puccinialin)<br><sub>Rust downloaded only to build some Python packages. Downloaded again if needed.</sub> | `~/Library/Caches/puccinialin` | 🟢 Recreates itself | By deleting it (to the Trash). |

## Build output

| Folder | Where | Verdict | How to free it |
|---|---|---|---|
| [Xcode build data](https://diskspaceai.com/folders/xcode-derived-data)<br><sub>Intermediate build results. Xcode recreates them.</sub> | `~/Library/Developer/Xcode/DerivedData` | 🟢 Recreates itself | By emptying the folder's contents (the folder stays). |

## Developer tools

| Folder | Where | Verdict | How to free it |
|---|---|---|---|
| [Xcode iOS symbols](https://diskspaceai.com/folders/xcode-device-support)<br><sub>Debug data for iOS versions. Recreated when you connect an iPhone.</sub> | `~/Library/Developer/Xcode/iOS DeviceSupport` | 🟢 Recreates itself | By emptying the folder's contents (the folder stays). |
| [Playwright browsers](https://diskspaceai.com/folders/playwright-browsers)<br><sub>Browsers for automated tests. Downloaded again with npx playwright install.</sub> | `~/Library/Caches/ms-playwright` | 🟢 Recreates itself | By emptying the folder's contents (the folder stays). |
| [Puppeteer browsers](https://diskspaceai.com/folders/puppeteer-browsers)<br><sub>Chrome downloaded by Puppeteer. Downloaded again when used.</sub> | `~/.cache/puppeteer` | 🟢 Recreates itself | By emptying the folder's contents (the folder stays). |
| [Prisma engines](https://diskspaceai.com/folders/prisma-engines)<br><sub>Prisma binaries. Downloaded again when you generate the client.</sub> | `~/.cache/prisma` | 🟢 Recreates itself | By emptying the folder's contents (the folder stays). |
| [Android Studio cache](https://diskspaceai.com/folders/android-studio-cache)<br><sub>Android Studio indexes and caches. Recreated when you open it.</sub> | `~/Library/Caches/Google/AndroidStudio*` | 🟢 Recreates itself | By deleting it (to the Trash). |
| [iPhone simulators](https://diskspaceai.com/folders/ios-simulators)<br><sub>Each simulator keeps the apps and data from your tests. Xcode creates them again.</sub> | `~/Library/Developer/CoreSimulator/Devices` | 🟠 Review | Delete them one by one in DiskSpace AI or in Xcode → Devices and Simulators. |
| [Xcode archives](https://diskspaceai.com/folders/xcode-archives)<br><sub>Released versions of your apps. Needed to read crash reports.</sub> | `~/Library/Developer/Xcode/Archives` | 🟠 Review | Delete old ones from Xcode → Organizer. |
| [Android SDK](https://diskspaceai.com/folders/android-sdk)<br><sub>Android platforms and tools.</sub> | `~/Library/Android/sdk` | 🟠 Review | Remove versions you don't use from Android Studio → SDK Manager. |
| [Android emulators](https://diskspaceai.com/folders/android-emulators)<br><sub>Each emulator keeps its own disk.</sub> | `~/.android/avd` | 🟠 Review | Delete the ones you don't use from Android Studio → Device Manager. |
| [Global npm packages](https://diskspaceai.com/folders/npm-global)<br><sub>Terminal tools installed with npm install -g. See which you have with npm ls -g --depth=0.</sub> | `~/.npm-global` | 🟠 Review | With the tool's own command: `npm uninstall -g ` |
| [uv Python versions](https://diskspaceai.com/folders/uv-python)<br><sub>Python versions installed by uv. Your projects' .venv environments depend on them. See which you have with uv python list.</sub> | `~/.local/share/uv/python` | 🟠 Review | With the tool's own command: `uv python uninstall ` |

## AI models

| Folder | Where | Verdict | How to free it |
|---|---|---|---|
| [Hugging Face models](https://diskspaceai.com/folders/huggingface)<br><sub>Downloaded AI models. They can be downloaded again, but they're big.</sub> | `~/.cache/huggingface` | 🟠 Review | huggingface-cli delete-cache (lets you choose which models to delete). |
| [Ollama models](https://diskspaceai.com/folders/ollama)<br><sub>Local AI models. See which you use with ollama list.</sub> | `~/.ollama/models` | 🟠 Review | With the tool's own command: `ollama rm ` |
| [LM Studio models](https://diskspaceai.com/folders/lmstudio)<br><sub>Local AI models downloaded from LM Studio.</sub> | `~/.lmstudio/models` | 🟠 Review | Delete the ones you don't use from LM Studio → My Models. |
| [Whisper models](https://diskspaceai.com/folders/whisper)<br><sub>Speech-to-text models. Downloaded again when used.</sub> | `~/.cache/whisper` | 🟠 Review | By emptying the folder's contents (the folder stays). |
| [PyTorch models](https://diskspaceai.com/folders/torch)<br><sub>Model weights downloaded by PyTorch.</sub> | `~/.cache/torch` | 🟠 Review | By emptying the folder's contents (the folder stays). |
| [Chroma models](https://diskspaceai.com/folders/chroma)<br><sub>Embedding models downloaded by Chroma.</sub> | `~/.cache/chroma` | 🟠 Review | By emptying the folder's contents (the folder stays). |
| [Chrome AI model](https://diskspaceai.com/folders/chrome-ai-model)<br><sub>Gemini Nano, which Chrome downloads by itself. It comes back unless you turn it off in chrome://flags.</sub> | `~/Library/Application Support/Google/Chrome/OptGuideOnDeviceModel` | 🟠 Review | Quit Google Chrome first. By deleting it (to the Trash). |

## AI apps and tools

| Folder | Where | Verdict | How to free it |
|---|---|---|---|
| [Codex runtimes](https://diskspaceai.com/folders/codex-runtimes)<br><sub>Codex runtime environments. Downloaded again when you open it.</sub> | `~/.cache/codex-runtimes` | 🟢 Recreates itself | By emptying the folder's contents (the folder stays). |
| [Claude app cache](https://diskspaceai.com/folders/claude-app-cache)<br><sub>Interface cache. Rebuilt automatically; quit the app first.</sub> | `~/Library/Application Support/Claude/Cache, Code Cache, GPUCache` | 🟢 Recreates itself | Quit Claude first. By deleting it (to the Trash). |
| [Old Claude Code versions](https://diskspaceai.com/folders/claude-code-old-versions)<br><sub>The Claude app downloads every new Claude Code version but only uses the latest.</sub> | `~/Library/Application Support/Claude/claude-code/<old versions>` | 🟢 Recreates itself | By deleting it (to the Trash). |
| [Codex temporary files](https://diskspaceai.com/folders/codex-tmp)<br><sub>Temporary files from Codex.</sub> | `~/.codex/.tmp` | 🟢 Recreates itself | By emptying the folder's contents (the folder stays). |
| [claude-mem logs](https://diskspaceai.com/folders/claude-mem-logs)<br><sub>Logs from the claude-mem memory plugin.</sub> | `~/.claude-mem/logs` | 🟢 Recreates itself | By emptying the folder's contents (the folder stays). |
| [Kimi cache](https://diskspaceai.com/folders/kimi-cache)<br><sub>Kimi's interface cache. Rebuilt automatically; quit the app first.</sub> | `~/Library/Application Support/kimi-desktop/Cache, Code Cache, GPUCache, DawnGraphiteCache, DawnWebGPUCache` | 🟢 Recreates itself | Quit Kimi first. By deleting it (to the Trash). |
| [Claude virtual machine](https://diskspaceai.com/folders/claude-vm)<br><sub>Used by the Claude app to run tasks. Downloaded again; quit the app first.</sub> | `~/Library/Application Support/Claude/vm_bundles` | 🟠 Review | Quit Claude first. By deleting it (to the Trash). |
| [Claude Code plugins](https://diskspaceai.com/folders/claude-code-plugins)<br><sub>Plugins installed in Claude Code. If you delete them, you'll have to reinstall them.</sub> | `~/.claude/plugins/cache` | 🟠 Review | Uninstall the ones you don't use with /plugin in Claude Code. |
| [claude-mem search index](https://diskspaceai.com/folders/claude-mem-index)<br><sub>Index for searching claude-mem's memory; rebuilt from its database.</sub> | `~/.claude-mem/chroma` | 🟠 Review | By deleting it (to the Trash). |
| [MiniMax agents](https://diskspaceai.com/folders/minimax-agents)<br><sub>Data and settings for MiniMax Agent's agents.</sub> | `~/.minimax/agents` | 🟠 Review | Review it in MiniMax Agent. |
| [Claude Code (version in use)](https://diskspaceai.com/folders/claude-code-current)<br><sub>The Claude Code version the Claude app is using right now.</sub> | `~/Library/Application Support/Claude/claude-code/<current version>` | ⚪ Your data | This is the version in use. |

## Virtual machines and containers

| Folder | Where | Verdict | How to free it |
|---|---|---|---|
| [Docker virtual disk](https://diskspaceai.com/folders/docker-disk)<br><sub>Images, containers and volumes. Volumes can hold databases.</sub> | `~/Library/Containers/com.docker.docker/Data/vms/0/data/Docker.raw` | 🟠 Review | With the tool's own command: `docker system prune -f` |
| [OrbStack data](https://diskspaceai.com/folders/orbstack)<br><sub>OrbStack machines and containers.</sub> | `~/.orbstack` | 🟠 Review | With the tool's own command: `docker system prune -f` |

## App caches

| Folder | Where | Verdict | How to free it |
|---|---|---|---|
| [Old update installers](https://diskspaceai.com/folders/app-updaters)<br><sub>App updates that were already installed (Kimi, MiniMax, Electron…).</sub> | `~/Library/Caches/*ShipIt, *updater*, *Updater*` | 🟢 Recreates itself | By deleting it (to the Trash). |
| [Downloaded Google updates](https://diskspaceai.com/folders/google-updater-cache)<br><sub>Packages the Chrome updater already installed.</sub> | `~/Library/Application Support/Google/GoogleUpdater/crx_cache` | 🟢 Recreates itself | By emptying the folder's contents (the folder stays). |
| [Chrome web cache](https://diskspaceai.com/folders/chrome-cache)<br><sub>Pages and images saved by Chrome. Rebuilt as you browse; best with Chrome closed.</sub> | `~/Library/Caches/Google/Chrome` | 🟢 Recreates itself | Quit Google Chrome first. By emptying the folder's contents (the folder stays). |
| [Unfinished Docker install](https://diskspaceai.com/folders/docker-install-leftover)<br><sub>Leftovers from a Docker Desktop install or update that already finished; quit Docker first.</sub> | `~/Library/Application Support/com.docker.install/in_progress` | 🟢 Recreates itself | Quit Docker Desktop first. By deleting it (to the Trash). |
| [App logs](https://diskspaceai.com/folders/user-logs)<br><sub>Log files. Only useful for diagnosing past errors.</sub> | `~/Library/Logs` | 🟢 Recreates itself | By emptying the folder's contents (the folder stays). |
| [Aerial wallpapers](https://diskspaceai.com/folders/aerial-wallpapers)<br><sub>Videos for macOS aerial wallpapers and screen savers. The one you pick is downloaded again.</sub> | `~/Library/Application Support/com.apple.wallpaper/aerials/videos` | 🟠 Review | By emptying the folder's contents (the folder stays). |
| [Slack cache](https://diskspaceai.com/folders/cache-slack)<br><sub>Slack's interface cache: pages, images and code it already loaded. It rebuilds itself when you open the app; your messages, sessions and settings aren't here.</sub> | `~/Library/Application Support/Slack/Cache, Code Cache, GPUCache` | 🟢 Recreates itself | Quit Slack first. By deleting it (to the Trash). |
| [Discord cache](https://diskspaceai.com/folders/cache-discord)<br><sub>Discord's interface cache: pages, images and code it already loaded. It rebuilds itself when you open the app; your messages, sessions and settings aren't here.</sub> | `~/Library/Application Support/discord/Cache, Code Cache, GPUCache` | 🟢 Recreates itself | Quit Discord first. By deleting it (to the Trash). |
| [Visual Studio Code cache](https://diskspaceai.com/folders/cache-vscode)<br><sub>Visual Studio Code's interface cache: pages, images and code it already loaded. It rebuilds itself when you open the app; your messages, sessions and settings aren't here.</sub> | `~/Library/Application Support/Code/Cache, Code Cache, GPUCache` | 🟢 Recreates itself | Quit Visual Studio Code first. By deleting it (to the Trash). |
| [Cursor cache](https://diskspaceai.com/folders/cache-cursor)<br><sub>Cursor's interface cache: pages, images and code it already loaded. It rebuilds itself when you open the app; your messages, sessions and settings aren't here.</sub> | `~/Library/Application Support/Cursor/Cache, Code Cache, GPUCache` | 🟢 Recreates itself | Quit Cursor first. By deleting it (to the Trash). |
| [Notion cache](https://diskspaceai.com/folders/cache-notion)<br><sub>Notion's interface cache: pages, images and code it already loaded. It rebuilds itself when you open the app; your messages, sessions and settings aren't here.</sub> | `~/Library/Application Support/Notion/Cache, Code Cache, GPUCache` | 🟢 Recreates itself | Quit Notion first. By deleting it (to the Trash). |
| [Figma cache](https://diskspaceai.com/folders/cache-figma)<br><sub>Figma's interface cache: pages, images and code it already loaded. It rebuilds itself when you open the app; your messages, sessions and settings aren't here.</sub> | `~/Library/Application Support/Figma/Cache, Code Cache, GPUCache` | 🟢 Recreates itself | Quit Figma first. By deleting it (to the Trash). |
| [Obsidian cache](https://diskspaceai.com/folders/cache-obsidian)<br><sub>Obsidian's interface cache: pages, images and code it already loaded. It rebuilds itself when you open the app; your messages, sessions and settings aren't here.</sub> | `~/Library/Application Support/obsidian/Cache, Code Cache, GPUCache` | 🟢 Recreates itself | Quit Obsidian first. By deleting it (to the Trash). |
| [Postman cache](https://diskspaceai.com/folders/cache-postman)<br><sub>Postman's interface cache: pages, images and code it already loaded. It rebuilds itself when you open the app; your messages, sessions and settings aren't here.</sub> | `~/Library/Application Support/Postman/Cache, Code Cache, GPUCache` | 🟢 Recreates itself | Quit Postman first. By deleting it (to the Trash). |
| [Linear cache](https://diskspaceai.com/folders/cache-linear)<br><sub>Linear's interface cache: pages, images and code it already loaded. It rebuilds itself when you open the app; your messages, sessions and settings aren't here.</sub> | `~/Library/Application Support/Linear/Cache, Code Cache, GPUCache` | 🟢 Recreates itself | Quit Linear first. By deleting it (to the Trash). |
| [Signal cache](https://diskspaceai.com/folders/cache-signal)<br><sub>Signal's interface cache: pages, images and code it already loaded. It rebuilds itself when you open the app; your messages, sessions and settings aren't here.</sub> | `~/Library/Application Support/Signal/Cache, Code Cache, GPUCache` | 🟢 Recreates itself | Quit Signal first. By deleting it (to the Trash). |

## Downloads

| Folder | Where | Verdict | How to free it |
|---|---|---|---|
| [Installers already used](https://diskspaceai.com/folders/used-installers)<br><sub>Installers of apps you already have installed and archives you already extracted: what they contained is already on your Mac. If you ever need them, they can be downloaded again.</sub> | `~/Downloads/<installers of installed apps and already extracted archives>` | 🟢 Recreates itself | By deleting it (to the Trash). |
| [Installers in Downloads](https://diskspaceai.com/folders/downloaded-installers)<br><sub>Downloaded installers and archives. Usually no longer needed.</sub> | `~/Downloads/*.dmg, *.pkg, *.zip, *.iso, *.xip` | 🟠 Review | By deleting it (to the Trash). |

## Your data

| Folder | Where | Verdict | How to free it |
|---|---|---|---|
| [iPhone backups](https://diskspaceai.com/folders/ios-backups)<br><sub>Local backups of your devices.</sub> | `~/Library/Application Support/MobileSync/Backup` | 🟠 Review | Manage from Finder → your iPhone → Manage Backups. |
| [Desktop screenshots](https://diskspaceai.com/folders/desktop-screenshots)<br><sub>Screenshots and screen recordings macOS saves on the Desktop. Check whether you need any: the ones you clean are kept 7 days.</sub> | `~/Desktop/Captura de pantalla *, Screenshot *, Grabación de pantalla *, Screen Recording *, CleanShot *` | 🟠 Review | By deleting it (to the Trash). |
| [Trash](https://diskspaceai.com/folders/trash)<br><sub>Files you already deleted.</sub> | `~/.Trash` | 🟠 Review | Empty the Trash from the Finder. |
| [Chrome profiles](https://diskspaceai.com/folders/chrome-profiles)<br><sub>History, sessions and extensions.</sub> | `~/Library/Application Support/Google/Chrome/Default, Profile *` | ⚪ Your data | This is your browsing data. |
| [Photos library](https://diskspaceai.com/folders/photos-library)<br><sub>Your photos and videos.</sub> | `~/Pictures/*.photoslibrary` | ⚪ Your data | Photos → Settings → iCloud → Optimize Mac Storage. |
| [Claude Code history](https://diskspaceai.com/folders/claude-code-history)<br><sub>Your Claude Code conversations, by project.</sub> | `~/.claude/projects` | ⚪ Your data | These are your conversations. |
| [Codex history](https://diskspaceai.com/folders/codex-sessions)<br><sub>Your Codex sessions.</sub> | `~/.codex/sessions` | ⚪ Your data | These are your sessions. |
| [claude-mem memory](https://diskspaceai.com/folders/claude-mem-memory)<br><sub>The database with the memory saved by the claude-mem plugin.</sub> | `~/.claude-mem/claude-mem.db*` | ⚪ Your data | This is your saved memory. |
