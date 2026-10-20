# DiskSpace AI para tu agente de IA (servidor MCP)

DiskSpace AI trae un servidor [MCP](https://modelcontextprotocol.io): tu agente (Claude Code, Claude Desktop, Codex, Cursor…) puede analizar el disco de tu Mac, ver qué hay en cada carpeta, explicar las que no se conocen y proponer una limpieza segura. Para limpiar siempre te pide permiso.

> «Hazme 20 GB de sitio, que tengo que actualizar macOS.»
>
> Puedo liberar **21,4 GB sin riesgo**: 9,4 GB de compilaciones de Xcode, 6,8 GB de la caché de uv y 5,2 GB de node_modules de proyectos parados. Tu Docker y tus fotos no los toco. ¿Lo hago?

## Conectar con un clic

1. [Descarga DiskSpace AI](https://diskspaceai.com/descargas/DiskSpaceAI.dmg) (1.0.5 o posterior) y ábrela.
2. Abre **Ajustes → IA → Conectar con tu agente de IA** y pulsa **Conectar** en Claude Code o Claude Desktop. No hace falta terminal; Claude Code también funciona dentro de la app de escritorio de Claude.
3. Abre una sesión nueva y pregunta «¿qué ocupa espacio en mi Mac?».

## Otros agentes

El servidor es el comando `diskspace` que va dentro de la app, con el argumento `mcp` (stdio).

**Claude Code** (terminal):

```bash
claude mcp add diskspace-ai -- "/Applications/DiskSpace AI.app/Contents/MacOS/diskspace" mcp
```

**Codex:**

```bash
codex mcp add diskspace-ai -- "/Applications/DiskSpace AI.app/Contents/MacOS/diskspace" mcp
```

**Cursor, Windsurf y cualquier otro con configuración JSON:**

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

## Herramientas

| Herramienta | Qué hace | |
|---|---|---|
| `analyze_disk` | Espacio libre y cada carpeta conocida con su tamaño, qué es, si es segura de borrar (safe / review / keep) y cómo se limpia. También dependencias de proyectos y carpetas sin clasificar. | Solo lee |
| `folder_contents` | Qué hay dentro de una carpeta, a dos niveles, con tamaños reales; salta las carpetas que solo envuelven otra. | Solo lee |
| `explain_folder` | Explica una carpeta desconocida con la IA de Apple, en el Mac. Nunca la da por segura. | Solo lee |
| `plan_cleanup` | Simulacro: qué se limpiaría y por qué se salta lo demás. | Solo lee |
| `clean` | Limpia los elementos elegidos. Exige `confirm: true`. | Pide permiso |
| `undo_last_cleanup` | Devuelve a su sitio lo que apartó la última limpieza. | Deshace |

## Garantías

- **Nunca limpia sin tu permiso**: `clean` exige confirmación explícita y el servidor le indica al agente que te enseñe el plan antes.
- **Lo tuyo se aparta 7 días**: solo se borra al momento lo que se regenera solo; lo demás se puede deshacer.
- **Las mismas reglas que la app**: tus carpetas protegidas en Ajustes no se tocan, ni lo de apps abiertas.
- **Analizar es gratis; limpiar es Pro** (gratis durante la beta).

## Privacidad

El servidor funciona entero en tu Mac y solo habla con el agente que tienes abierto. Si tu agente usa un modelo en la nube, ese servicio ve lo que DiskSpace AI le responde (nombres de carpetas, rutas y tamaños, nunca el contenido de tus archivos), según su propia política de privacidad.

## Prueba a pedirle

- «¿Qué ocupa espacio en mi Mac?»
- «Hazme 20 GB de sitio sin tocar mis archivos.»
- «¿Qué hay dentro de mis simuladores de Xcode?»
- «Limpia las cachés de desarrollo y enséñame el plan antes.»

Más información: [diskspaceai.com/es/mcp](https://diskspaceai.com/es/mcp)
