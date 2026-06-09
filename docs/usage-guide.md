# Usage Guide — AutoTyper Tool

A complete guide to using **AutoTyper Tool**: hotkeys, settings, presets, configuration files, and tips for getting natural-looking, reliable automatic typing.

## Table of Contents

- [Quick Start](#quick-start)
- [Main Window Overview](#main-window-overview)
- [Hotkeys Reference](#hotkeys-reference)
- [Typing Settings Explained](#typing-settings-explained)
- [Loading Text From a File](#loading-text-from-a-file)
- [Presets](#presets)
- [Configuration File Format](#configuration-file-format)
- [Running AutoTyper Tool at Startup](#running-autotyper-tool-at-startup)
- [Tips for Natural-Looking Typing](#tips-for-natural-looking-typing)
- [Troubleshooting](#troubleshooting)

## Quick Start

1. Launch `AutoTyper.exe`.
2. Type or paste your text into the main editor.
3. Click into the target window (browser, document, chat, etc.).
4. Press **`F6`** to start typing.
5. Press **`Esc`** to stop at any time.

## Main Window Overview

The main window is split into two areas:

- **Left panel — Text to type**: a multi-line text editor where you write or paste the content you want AutoTyper Tool to type. You can also load this from a `.txt` file.
- **Right panel — Settings**: typing speed, start delay, loop mode, hotkeys, and the "humanize" random delay toggle.

A **Start Typing** button mirrors the `F6` hotkey, and a status bar at the bottom shows progress (`Characters typed: X / Y`) and current speed.

## Hotkeys Reference

| Action | Default | Notes |
|---|---|---|
| Start / Resume | `F6` | Begins typing at the current cursor position in the focused window |
| Pause | `F7` | Pauses without losing your place; press again to resume |
| Stop | `Esc` | Immediately cancels typing |
| Open Settings | `Ctrl + ,` | Opens the settings panel |
| Load Text File | `Ctrl + O` | Opens a file picker for `.txt` files |
| Save Preset | `Ctrl + S` | Saves the current configuration |

To change a hotkey: open **Settings → Hotkeys**, click the field next to the action, and press your desired key combination.

## Typing Settings Explained

| Setting | Description |
|---|---|
| **Typing Speed (CPS)** | Characters per second. Higher values type faster. Range: 1–500. |
| **Start Delay** | Number of seconds to wait after pressing the start hotkey before typing begins — gives you time to click into the target window. |
| **Random Delay (Humanize)** | When enabled, adds a small random variation (in milliseconds) to the delay between each keystroke, making the typing pattern look more human. |
| **Repeat / Loop** | `Off` types the text once. `N times` repeats it a fixed number of times. `Infinite` repeats until you press `Esc`. |
| **New-Line Handling** | Controls how line breaks (`\n`) in your text are sent: as `Enter`, as `Shift+Enter` (useful for chat apps where `Enter` sends the message), or skipped entirely. |

## Loading Text From a File

1. Click **Load File** (or press `Ctrl + O`).
2. Select any `.txt` file.
3. Its contents will replace the text editor's content.

This is useful for typing long scripts, articles, code snippets, or multi-line forms.

## Presets

Presets let you save a full configuration (text, speed, delay, hotkeys, loop settings) and reload it later.

- **Save**: `Ctrl + S`, then give your preset a name.
- **Load**: Settings → Presets → select a saved preset.

Presets are stored as `.json` files — see [scripts/example-config.json](../scripts/example-config.json) for the format.

## Configuration File Format

AutoTyper Tool presets are plain JSON files with the following structure:

```json
{
  "name": "My Preset",
  "text": "Hello, this will be typed automatically!",
  "typingSpeedCps": 80,
  "startDelaySeconds": 3,
  "humanizeDelay": false,
  "loopMode": "off",
  "loopCount": 1,
  "newLineMode": "enter",
  "hotkeys": {
    "start": "F6",
    "pause": "F7",
    "stop": "Escape"
  }
}
```

You can hand-edit these files or generate them with the example script in [scripts/autotype_cli.py](../scripts/autotype_cli.py).

## Running AutoTyper Tool at Startup

To launch AutoTyper Tool automatically when Windows starts:

1. Press `Win + R`, type `shell:startup`, and press Enter. This opens your Startup folder.
2. Right-click `AutoTyper.exe` and choose **"Create shortcut"**.
3. Move (or copy) that shortcut into the Startup folder you opened in step 1.

AutoTyper Tool will now launch automatically (minimized to the system tray, if enabled in Settings) every time you log in.

## Tips for Natural-Looking Typing

- Enable **Random Delay (Humanize)** to avoid perfectly uniform keystroke timing.
- Use a **Start Delay** of at least 2–3 seconds to ensure the target window has focus.
- For chat apps where `Enter` sends a message, set **New-Line Handling** to `Shift+Enter` so multi-line messages aren't sent prematurely.
- Lower the **Typing Speed** for more readable "live typing" effects in screen recordings.

## Troubleshooting

**Nothing happens when I press F6.**
Make sure the target window is focused (clicked into) before pressing the hotkey, and check that another application isn't using the same global hotkey.

**Special characters or accents aren't typed correctly.**
Ensure your Windows keyboard layout matches the language of the text you're typing — AutoTyper Tool uses Unicode input, but some applications interpret layout-dependent key codes differently.

**AutoTyper Tool won't start (SmartScreen / antivirus).**
See [Installation Guide → Windows SmartScreen Warning](installation.md#windows-smartscreen-warning) and [Antivirus False Positives](installation.md#antivirus-false-positives).

**Typing is too fast/slow for the target app.**
Some web forms and games throttle input events. Lower the **Typing Speed (CPS)** value if characters are being dropped.

---

See also: [Installation Guide](installation.md) · [Extended FAQ](faq.md) · [Changelog](../CHANGELOG.md)
