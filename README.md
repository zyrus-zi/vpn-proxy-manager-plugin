# VPN Proxy Manager

[🇷🇺 Русская версия](README.ru.md)

A plugin for [exteraGram](https://exteragram.app) and [AyuGram](https://ayugram.one) that automatically disables the proxy when a VPN is active on the device, and re-enables it when the VPN disconnects.

---

## How it works

The plugin runs a background monitor that checks every 3 seconds whether a VPN connection is active using Android's `ConnectivityManager`. When the state changes:

| Event | Action |
|---|---|
| VPN **connected** | Proxy is **disabled** |
| VPN **disconnected** | Proxy is **restored** (only if it was disabled by this plugin) |

---

## Features

- 🔄 Automatic proxy management based on VPN state
- 🔔 In-app bulletin notifications when proxy state changes
- ⚙️ Toggle auto-management directly from plugin settings
- 🛡 Safe restore — only re-enables proxy if the plugin itself disabled it

---

## Installation

1. Download the latest `.plugin` file from [Releases](../../releases)
2. Open exteraGram or AyuGram
3. Go to **Settings → Plugins → Install from file**
4. Select the downloaded file and enable the plugin

---

## Requirements

- exteraGram `11.12.0`+ or AyuGram (full version only — Lite does not support plugins)
- A proxy must be configured in Telegram settings beforehand

---

## Settings

| Setting | Description | Default |
|---|---|---|
| Auto-manage proxy | Enable/disable the core functionality | ✅ On |
| Show notifications | Show bulletin when proxy state changes | ✅ On |
| Button in side menu | Quick toggle in the drawer menu | ✅ On |

---

## Compatibility

| App | Supported | Side menu button |
|---|---|---|
| exteraGram | ✅ | ✅ up to 12.2.10 |
| AyuGram | ✅ | ✅ 12.2.10 |

---

## Author

[@zyrus-zi](https://github.com/zyrus-zi)

---

## License

[MIT](LICENSE)
