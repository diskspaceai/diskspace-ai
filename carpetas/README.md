# Qué es cada carpeta de tu Mac y si se puede borrar

Las 73 carpetas y cachés que conoce DiskSpace AI. **Se regenera solo**: la herramienta que lo creó lo vuelve a crear. **Revisar**: puede guardar algo tuyo. **Tus datos**: no se borra. Cada una tiene su página en la [guía de la web](https://diskspaceai.com/es/carpetas).

También en [JSON](carpetas.json), para usarlo en tus scripts. ¿Falta alguna? [Abre una incidencia](../../../issues/new/choose).

## Cachés de paquetes

| Carpeta | Dónde | Veredicto | Cómo liberarla |
|---|---|---|---|
| [Caché de uv (Python)](https://diskspaceai.com/es/carpetas/uv-cache)<br><sub>Paquetes de Python que uv ya descargó. Los vuelve a bajar cuando hacen falta.</sub> | `~/.cache/uv` | 🟢 Se regenera solo | Con el comando de la propia herramienta: `uv cache clean` |
| [Caché de pip](https://diskspaceai.com/es/carpetas/pip-cache)<br><sub>Paquetes de Python descargados por pip.</sub> | `~/Library/Caches/pip` | 🟢 Se regenera solo | Con el comando de la propia herramienta: `pip cache purge` |
| [Caché de npm](https://diskspaceai.com/es/carpetas/npm-cache)<br><sub>Copias de paquetes que npm ya instaló. Los vuelve a descargar si hacen falta.</sub> | `~/.npm/_cacache` | 🟢 Se regenera solo | Con el comando de la propia herramienta: `npm cache clean --force` |
| [Paquetes temporales de npx](https://diskspaceai.com/es/carpetas/npx-cache)<br><sub>Herramientas que npx descargó para ejecutarlas una vez.</sub> | `~/.npm/_npx` | 🟢 Se regenera solo | Vaciando el contenido de la carpeta (la carpeta se queda). |
| [Almacén de pnpm](https://diskspaceai.com/es/carpetas/pnpm-store)<br><sub>Paquetes compartidos por tus proyectos. «prune» solo quita los que ya no usa ninguno.</sub> | `~/Library/pnpm/store` | 🟢 Se regenera solo | Con el comando de la propia herramienta: `pnpm store prune` |
| [Caché de pnpm](https://diskspaceai.com/es/carpetas/pnpm-cache)<br><sub>Metadatos de paquetes descargados por pnpm.</sub> | `~/Library/Caches/pnpm` | 🟢 Se regenera solo | Vaciando el contenido de la carpeta (la carpeta se queda). |
| [Caché de Yarn](https://diskspaceai.com/es/carpetas/yarn-cache)<br><sub>Paquetes descargados por Yarn.</sub> | `~/Library/Caches/Yarn` | 🟢 Se regenera solo | Con el comando de la propia herramienta: `yarn cache clean` |
| [Caché de Bun](https://diskspaceai.com/es/carpetas/bun-cache)<br><sub>Paquetes descargados por Bun.</sub> | `~/.bun/install/cache` | 🟢 Se regenera solo | Con el comando de la propia herramienta: `bun pm cache rm` |
| [Caché de Homebrew](https://diskspaceai.com/es/carpetas/homebrew-cache)<br><sub>Instaladores de programas que Homebrew ya instaló.</sub> | `~/Library/Caches/Homebrew` | 🟢 Se regenera solo | Con el comando de la propia herramienta: `brew cleanup -s` |
| [Caché de Gradle](https://diskspaceai.com/es/carpetas/gradle-cache)<br><sub>Dependencias de proyectos Android y Java. La próxima compilación tardará más.</sub> | `~/.gradle/caches` | 🟢 Se regenera solo | Vaciando el contenido de la carpeta (la carpeta se queda). |
| [Versiones de Gradle descargadas](https://diskspaceai.com/es/carpetas/gradle-wrapper)<br><sub>Cada proyecto descarga la versión de Gradle que pide. Se vuelve a bajar al compilar.</sub> | `~/.gradle/wrapper/dists` | 🟢 Se regenera solo | Vaciando el contenido de la carpeta (la carpeta se queda). |
| [Rust temporal para paquetes de Python](https://diskspaceai.com/es/carpetas/puccinialin)<br><sub>Rust que se descarga solo para compilar algunos paquetes de Python. Se vuelve a bajar si hace falta.</sub> | `~/Library/Caches/puccinialin` | 🟢 Se regenera solo | Borrándola (a la papelera). |

## Compilaciones

| Carpeta | Dónde | Veredicto | Cómo liberarla |
|---|---|---|---|
| [Compilaciones de Xcode](https://diskspaceai.com/es/carpetas/xcode-derived-data)<br><sub>Resultados intermedios de compilar. Xcode los regenera.</sub> | `~/Library/Developer/Xcode/DerivedData` | 🟢 Se regenera solo | Vaciando el contenido de la carpeta (la carpeta se queda). |

## Herramientas de desarrollo

| Carpeta | Dónde | Veredicto | Cómo liberarla |
|---|---|---|---|
| [Símbolos de iOS de Xcode](https://diskspaceai.com/es/carpetas/xcode-device-support)<br><sub>Datos de depuración de versiones de iOS. Se regeneran al conectar un iPhone.</sub> | `~/Library/Developer/Xcode/iOS DeviceSupport` | 🟢 Se regenera solo | Vaciando el contenido de la carpeta (la carpeta se queda). |
| [Navegadores de Playwright](https://diskspaceai.com/es/carpetas/playwright-browsers)<br><sub>Navegadores para tests automáticos. Se vuelven a bajar con npx playwright install.</sub> | `~/Library/Caches/ms-playwright` | 🟢 Se regenera solo | Vaciando el contenido de la carpeta (la carpeta se queda). |
| [Navegadores de Puppeteer](https://diskspaceai.com/es/carpetas/puppeteer-browsers)<br><sub>Chrome descargado por Puppeteer. Se vuelve a bajar al usarlo.</sub> | `~/.cache/puppeteer` | 🟢 Se regenera solo | Vaciando el contenido de la carpeta (la carpeta se queda). |
| [Motores de Prisma](https://diskspaceai.com/es/carpetas/prisma-engines)<br><sub>Binarios de Prisma. Se descargan de nuevo al generar el cliente.</sub> | `~/.cache/prisma` | 🟢 Se regenera solo | Vaciando el contenido de la carpeta (la carpeta se queda). |
| [Caché de Android Studio](https://diskspaceai.com/es/carpetas/android-studio-cache)<br><sub>Índices y cachés de Android Studio. Se regeneran al abrirlo.</sub> | `~/Library/Caches/Google/AndroidStudio*` | 🟢 Se regenera solo | Borrándola (a la papelera). |
| [Caché de generate_appcast (Sparkle)](https://diskspaceai.com/es/carpetas/sparkle-appcast-cache)<br><sub>Copias que la herramienta generate_appcast de Sparkle descomprime para firmar actualizaciones. Las vuelve a crear la próxima vez.</sub> | `~/Library/Caches/Sparkle_generate_appcast` | 🟢 Se regenera solo | Borrándola (a la papelera). |
| [Caché de Python de Apple](https://diskspaceai.com/es/carpetas/apple-python-cache)<br><sub>Archivos .pyc que el Python de Xcode y de macOS compila para arrancar más rápido. Se regeneran solos.</sub> | `~/Library/Caches/com.apple.python` | 🟢 Se regenera solo | Borrándola (a la papelera). |
| [Simuladores de iPhone](https://diskspaceai.com/es/carpetas/ios-simulators)<br><sub>Cada simulador guarda las apps y datos de tus pruebas. Xcode los vuelve a crear.</sub> | `~/Library/Developer/CoreSimulator/Devices` | 🟠 Revisar | Bórralos uno a uno en DiskSpace AI o en Xcode → Devices and Simulators. |
| [Archivos de Xcode](https://diskspaceai.com/es/carpetas/xcode-archives)<br><sub>Versiones publicadas de tus apps. Sirven para leer informes de fallos.</sub> | `~/Library/Developer/Xcode/Archives` | 🟠 Revisar | Borrar las antiguas desde Xcode → Organizer. |
| [SDK de Android](https://diskspaceai.com/es/carpetas/android-sdk)<br><sub>Plataformas y herramientas de Android.</sub> | `~/Library/Android/sdk` | 🟠 Revisar | Quitar las versiones que no uses desde Android Studio → SDK Manager. |
| [Emuladores de Android](https://diskspaceai.com/es/carpetas/android-emulators)<br><sub>Cada emulador guarda su propio disco.</sub> | `~/.android/avd` | 🟠 Revisar | Borrar los que no uses desde Android Studio → Device Manager. |
| [Paquetes globales de npm](https://diskspaceai.com/es/carpetas/npm-global)<br><sub>Herramientas de terminal instaladas con npm install -g. Mira cuáles tienes con npm ls -g --depth=0.</sub> | `~/.npm-global` | 🟠 Revisar | Con el comando de la propia herramienta: `npm uninstall -g ` |
| [Versiones de Python de uv](https://diskspaceai.com/es/carpetas/uv-python)<br><sub>Pythons instalados por uv. Los entornos .venv de tus proyectos dependen de ellos. Mira cuáles tienes con uv python list.</sub> | `~/.local/share/uv/python` | 🟠 Revisar | Con el comando de la propia herramienta: `uv python uninstall ` |

## Modelos de IA

| Carpeta | Dónde | Veredicto | Cómo liberarla |
|---|---|---|---|
| [Modelos de Hugging Face](https://diskspaceai.com/es/carpetas/huggingface)<br><sub>Modelos de IA descargados. Se pueden volver a bajar, pero pesan mucho.</sub> | `~/.cache/huggingface` | 🟠 Revisar | huggingface-cli delete-cache (te deja elegir qué modelos borrar). |
| [Modelos de Ollama](https://diskspaceai.com/es/carpetas/ollama)<br><sub>Modelos de IA locales. Mira cuáles usas con ollama list.</sub> | `~/.ollama/models` | 🟠 Revisar | Con el comando de la propia herramienta: `ollama rm ` |
| [Modelos de LM Studio](https://diskspaceai.com/es/carpetas/lmstudio)<br><sub>Modelos de IA locales descargados desde LM Studio.</sub> | `~/.lmstudio/models` | 🟠 Revisar | Borrar los que no uses desde LM Studio → My Models. |
| [Modelos de Whisper](https://diskspaceai.com/es/carpetas/whisper)<br><sub>Modelos de transcripción de voz. Se descargan al volver a usarlos.</sub> | `~/.cache/whisper` | 🟠 Revisar | Vaciando el contenido de la carpeta (la carpeta se queda). |
| [Modelos de PyTorch](https://diskspaceai.com/es/carpetas/torch)<br><sub>Pesos de modelos descargados por PyTorch.</sub> | `~/.cache/torch` | 🟠 Revisar | Vaciando el contenido de la carpeta (la carpeta se queda). |
| [Modelos de Chroma](https://diskspaceai.com/es/carpetas/chroma)<br><sub>Modelos de embeddings que descarga Chroma.</sub> | `~/.cache/chroma` | 🟠 Revisar | Vaciando el contenido de la carpeta (la carpeta se queda). |
| [Modelo de IA de Chrome](https://diskspaceai.com/es/carpetas/chrome-ai-model)<br><sub>Gemini Nano, que Chrome descarga solo. Vuelve si no lo desactivas en chrome://flags.</sub> | `~/Library/Application Support/Google/Chrome/OptGuideOnDeviceModel` | 🟠 Revisar | Cierra Google Chrome antes. Borrándola (a la papelera). |

## Apps y herramientas de IA

| Carpeta | Dónde | Veredicto | Cómo liberarla |
|---|---|---|---|
| [Entornos de Codex](https://diskspaceai.com/es/carpetas/codex-runtimes)<br><sub>Entornos de ejecución de Codex. Se descargan de nuevo al abrirlo.</sub> | `~/.cache/codex-runtimes` | 🟢 Se regenera solo | Vaciando el contenido de la carpeta (la carpeta se queda). |
| [Caché de la app de Claude](https://diskspaceai.com/es/carpetas/claude-app-cache)<br><sub>Caché de la interfaz. Se reconstruye; cierra la app antes.</sub> | `~/Library/Application Support/Claude/Cache, Code Cache, GPUCache` | 🟢 Se regenera solo | Cierra Claude antes. Borrándola (a la papelera). |
| [Versiones antiguas de Claude Code](https://diskspaceai.com/es/carpetas/claude-code-old-versions)<br><sub>La app de Claude descarga cada versión nueva de Claude Code; solo usa la más reciente.</sub> | `~/Library/Application Support/Claude/claude-code/<versiones antiguas>` | 🟢 Se regenera solo | Borrándola (a la papelera). |
| [Temporales de Codex](https://diskspaceai.com/es/carpetas/codex-tmp)<br><sub>Archivos temporales de Codex.</sub> | `~/.codex/.tmp` | 🟢 Se regenera solo | Vaciando el contenido de la carpeta (la carpeta se queda). |
| [Registros de claude-mem](https://diskspaceai.com/es/carpetas/claude-mem-logs)<br><sub>Registros del plugin de memoria claude-mem.</sub> | `~/.claude-mem/logs` | 🟢 Se regenera solo | Vaciando el contenido de la carpeta (la carpeta se queda). |
| [Caché de Kimi](https://diskspaceai.com/es/carpetas/kimi-cache)<br><sub>Caché de la interfaz de Kimi. Se reconstruye; cierra la app antes.</sub> | `~/Library/Application Support/kimi-desktop/Cache, Code Cache, GPUCache, DawnGraphiteCache, DawnWebGPUCache` | 🟢 Se regenera solo | Cierra Kimi antes. Borrándola (a la papelera). |
| [Caché de Perplexity](https://diskspaceai.com/es/carpetas/perplexity-cache)<br><sub>Páginas e imágenes que guarda la app de Perplexity. Se reconstruye; cierra la app antes.</sub> | `~/Library/Caches/ai.perplexity.macv3` | 🟢 Se regenera solo | Cierra Perplexity antes. Vaciando el contenido de la carpeta (la carpeta se queda). |
| [Máquina virtual de Claude](https://diskspaceai.com/es/carpetas/claude-vm)<br><sub>La usa la app de Claude para ejecutar tareas. Se vuelve a descargar; cierra la app antes.</sub> | `~/Library/Application Support/Claude/vm_bundles` | 🟠 Revisar | Cierra Claude antes. Borrándola (a la papelera). |
| [Plugins de Claude Code](https://diskspaceai.com/es/carpetas/claude-code-plugins)<br><sub>Plugins instalados en Claude Code. Si los borras, hay que reinstalarlos.</sub> | `~/.claude/plugins/cache` | 🟠 Revisar | Desinstala los que no uses con /plugin en Claude Code. |
| [Índice de búsqueda de claude-mem](https://diskspaceai.com/es/carpetas/claude-mem-index)<br><sub>Índice para buscar en la memoria de claude-mem; se reconstruye desde su base de datos.</sub> | `~/.claude-mem/chroma` | 🟠 Revisar | Borrándola (a la papelera). |
| [Agentes de MiniMax](https://diskspaceai.com/es/carpetas/minimax-agents)<br><sub>Datos y configuración de los agentes de MiniMax Agent.</sub> | `~/.minimax/agents` | 🟠 Revisar | Revísalo desde MiniMax Agent. |
| [Claude Code (versión en uso)](https://diskspaceai.com/es/carpetas/claude-code-current)<br><sub>La versión de Claude Code que usa la app de Claude ahora mismo.</sub> | `~/Library/Application Support/Claude/claude-code/<versión en uso>` | ⚪ Tus datos | Es la versión en uso. |

## Máquinas virtuales y contenedores

| Carpeta | Dónde | Veredicto | Cómo liberarla |
|---|---|---|---|
| [Disco virtual de Docker](https://diskspaceai.com/es/carpetas/docker-disk)<br><sub>Imágenes, contenedores y volúmenes. Los volúmenes pueden guardar bases de datos.</sub> | `~/Library/Containers/com.docker.docker/Data/vms/0/data/Docker.raw` | 🟠 Revisar | Con el comando de la propia herramienta: `docker system prune -f` |
| [Datos de OrbStack](https://diskspaceai.com/es/carpetas/orbstack)<br><sub>Máquinas y contenedores de OrbStack.</sub> | `~/.orbstack` | 🟠 Revisar | Con el comando de la propia herramienta: `docker system prune -f` |

## Cachés de apps

| Carpeta | Dónde | Veredicto | Cómo liberarla |
|---|---|---|---|
| [Instaladores de actualizaciones viejas](https://diskspaceai.com/es/carpetas/app-updaters)<br><sub>Actualizaciones de apps que ya se instalaron (Kimi, MiniMax, Electron…).</sub> | `~/Library/Caches/*ShipIt, *updater*, *Updater*` | 🟢 Se regenera solo | Borrándola (a la papelera). |
| [Actualizaciones descargadas de Google](https://diskspaceai.com/es/carpetas/google-updater-cache)<br><sub>Paquetes que el actualizador de Chrome ya instaló.</sub> | `~/Library/Application Support/Google/GoogleUpdater/crx_cache` | 🟢 Se regenera solo | Vaciando el contenido de la carpeta (la carpeta se queda). |
| [Caché web de Chrome](https://diskspaceai.com/es/carpetas/chrome-cache)<br><sub>Páginas e imágenes guardadas por Chrome. Se reconstruye al navegar; mejor con Chrome cerrado.</sub> | `~/Library/Caches/Google/Chrome` | 🟢 Se regenera solo | Cierra Google Chrome antes. Vaciando el contenido de la carpeta (la carpeta se queda). |
| [Instalación de Docker a medias](https://diskspaceai.com/es/carpetas/docker-install-leftover)<br><sub>Restos de una instalación o actualización de Docker Desktop que ya terminó; cierra Docker antes.</sub> | `~/Library/Application Support/com.docker.install/in_progress` | 🟢 Se regenera solo | Cierra Docker antes. Borrándola (a la papelera). |
| [Registros de apps](https://diskspaceai.com/es/carpetas/user-logs)<br><sub>Archivos de registro. Solo sirven para diagnosticar errores pasados.</sub> | `~/Library/Logs` | 🟢 Se regenera solo | Vaciando el contenido de la carpeta (la carpeta se queda). |
| [Fondos de pantalla animados](https://diskspaceai.com/es/carpetas/aerial-wallpapers)<br><sub>Vídeos de los fondos y salvapantallas aéreos de macOS. Se vuelve a descargar el que elijas.</sub> | `~/Library/Application Support/com.apple.wallpaper/aerials/videos` | 🟠 Revisar | Vaciando el contenido de la carpeta (la carpeta se queda). |
| [Caché de Slack](https://diskspaceai.com/es/carpetas/cache-slack)<br><sub>Caché de la interfaz de Slack: páginas, imágenes y código ya cargados. Se reconstruye sola al abrir la app; tus mensajes, sesiones y ajustes no están aquí.</sub> | `~/Library/Application Support/Slack/Cache, Code Cache, GPUCache` | 🟢 Se regenera solo | Cierra Slack antes. Borrándola (a la papelera). |
| [Caché de Discord](https://diskspaceai.com/es/carpetas/cache-discord)<br><sub>Caché de la interfaz de Discord: páginas, imágenes y código ya cargados. Se reconstruye sola al abrir la app; tus mensajes, sesiones y ajustes no están aquí.</sub> | `~/Library/Application Support/discord/Cache, Code Cache, GPUCache` | 🟢 Se regenera solo | Cierra Discord antes. Borrándola (a la papelera). |
| [Caché de Visual Studio Code](https://diskspaceai.com/es/carpetas/cache-vscode)<br><sub>Caché de la interfaz de Visual Studio Code: páginas, imágenes y código ya cargados. Se reconstruye sola al abrir la app; tus mensajes, sesiones y ajustes no están aquí.</sub> | `~/Library/Application Support/Code/Cache, Code Cache, GPUCache` | 🟢 Se regenera solo | Cierra Visual Studio Code antes. Borrándola (a la papelera). |
| [Caché de Cursor](https://diskspaceai.com/es/carpetas/cache-cursor)<br><sub>Caché de la interfaz de Cursor: páginas, imágenes y código ya cargados. Se reconstruye sola al abrir la app; tus mensajes, sesiones y ajustes no están aquí.</sub> | `~/Library/Application Support/Cursor/Cache, Code Cache, GPUCache` | 🟢 Se regenera solo | Cierra Cursor antes. Borrándola (a la papelera). |
| [Caché de Notion](https://diskspaceai.com/es/carpetas/cache-notion)<br><sub>Caché de la interfaz de Notion: páginas, imágenes y código ya cargados. Se reconstruye sola al abrir la app; tus mensajes, sesiones y ajustes no están aquí.</sub> | `~/Library/Application Support/Notion/Cache, Code Cache, GPUCache` | 🟢 Se regenera solo | Cierra Notion antes. Borrándola (a la papelera). |
| [Caché de Figma](https://diskspaceai.com/es/carpetas/cache-figma)<br><sub>Caché de la interfaz de Figma: páginas, imágenes y código ya cargados. Se reconstruye sola al abrir la app; tus mensajes, sesiones y ajustes no están aquí.</sub> | `~/Library/Application Support/Figma/Cache, Code Cache, GPUCache` | 🟢 Se regenera solo | Cierra Figma antes. Borrándola (a la papelera). |
| [Caché de Obsidian](https://diskspaceai.com/es/carpetas/cache-obsidian)<br><sub>Caché de la interfaz de Obsidian: páginas, imágenes y código ya cargados. Se reconstruye sola al abrir la app; tus mensajes, sesiones y ajustes no están aquí.</sub> | `~/Library/Application Support/obsidian/Cache, Code Cache, GPUCache` | 🟢 Se regenera solo | Cierra Obsidian antes. Borrándola (a la papelera). |
| [Caché de Postman](https://diskspaceai.com/es/carpetas/cache-postman)<br><sub>Caché de la interfaz de Postman: páginas, imágenes y código ya cargados. Se reconstruye sola al abrir la app; tus mensajes, sesiones y ajustes no están aquí.</sub> | `~/Library/Application Support/Postman/Cache, Code Cache, GPUCache` | 🟢 Se regenera solo | Cierra Postman antes. Borrándola (a la papelera). |
| [Caché de Linear](https://diskspaceai.com/es/carpetas/cache-linear)<br><sub>Caché de la interfaz de Linear: páginas, imágenes y código ya cargados. Se reconstruye sola al abrir la app; tus mensajes, sesiones y ajustes no están aquí.</sub> | `~/Library/Application Support/Linear/Cache, Code Cache, GPUCache` | 🟢 Se regenera solo | Cierra Linear antes. Borrándola (a la papelera). |
| [Caché de Signal](https://diskspaceai.com/es/carpetas/cache-signal)<br><sub>Caché de la interfaz de Signal: páginas, imágenes y código ya cargados. Se reconstruye sola al abrir la app; tus mensajes, sesiones y ajustes no están aquí.</sub> | `~/Library/Application Support/Signal/Cache, Code Cache, GPUCache` | 🟢 Se regenera solo | Cierra Signal antes. Borrándola (a la papelera). |

## Descargas

| Carpeta | Dónde | Veredicto | Cómo liberarla |
|---|---|---|---|
| [Instaladores ya usados](https://diskspaceai.com/es/carpetas/used-installers)<br><sub>Instaladores de apps que ya tienes instaladas y comprimidos que ya descomprimiste: lo que contenían ya está en tu Mac. Si algún día los necesitas, se vuelven a descargar.</sub> | `~/Downloads/<instaladores de apps ya instaladas y comprimidos ya descomprimidos>` | 🟢 Se regenera solo | Borrándola (a la papelera). |
| [Instaladores en Descargas](https://diskspaceai.com/es/carpetas/downloaded-installers)<br><sub>Instaladores y archivos comprimidos descargados. Normalmente ya no hacen falta.</sub> | `~/Downloads/*.dmg, *.pkg, *.zip, *.iso, *.xip` | 🟠 Revisar | Borrándola (a la papelera). |

## Tus datos

| Carpeta | Dónde | Veredicto | Cómo liberarla |
|---|---|---|---|
| [Copias de seguridad del iPhone](https://diskspaceai.com/es/carpetas/ios-backups)<br><sub>Copias locales de tus dispositivos.</sub> | `~/Library/Application Support/MobileSync/Backup` | 🟠 Revisar | Gestionar desde Finder → tu iPhone → Gestionar copias. |
| [Capturas de pantalla del Escritorio](https://diskspaceai.com/es/carpetas/desktop-screenshots)<br><sub>Capturas y grabaciones de pantalla que macOS guarda en el Escritorio. Mira si alguna te hace falta: las que limpies se apartan 7 días.</sub> | `~/Desktop/Captura de pantalla *, Screenshot *, Grabación de pantalla *, Screen Recording *, CleanShot *` | 🟠 Revisar | Borrándola (a la papelera). |
| [Papelera](https://diskspaceai.com/es/carpetas/trash)<br><sub>Archivos que ya borraste.</sub> | `~/.Trash` | 🟠 Revisar | Vaciar la papelera desde el Finder. |
| [Perfiles de Chrome](https://diskspaceai.com/es/carpetas/chrome-profiles)<br><sub>Historial, sesiones y extensiones.</sub> | `~/Library/Application Support/Google/Chrome/Default, Profile *` | ⚪ Tus datos | Son tus datos de navegación. |
| [Fototeca](https://diskspaceai.com/es/carpetas/photos-library)<br><sub>Tus fotos y vídeos.</sub> | `~/Pictures/*.photoslibrary` | ⚪ Tus datos | Fotos → Ajustes → iCloud → Optimizar almacenamiento. |
| [Historial de Claude Code](https://diskspaceai.com/es/carpetas/claude-code-history)<br><sub>Tus conversaciones con Claude Code, por proyecto.</sub> | `~/.claude/projects` | ⚪ Tus datos | Son tus conversaciones. |
| [Historial de Codex](https://diskspaceai.com/es/carpetas/codex-sessions)<br><sub>Tus sesiones de Codex.</sub> | `~/.codex/sessions` | ⚪ Tus datos | Son tus sesiones. |
| [Memoria de claude-mem](https://diskspaceai.com/es/carpetas/claude-mem-memory)<br><sub>La base de datos con la memoria que guarda el plugin claude-mem.</sub> | `~/.claude-mem/claude-mem.db*` | ⚪ Tus datos | Es tu memoria guardada. |
