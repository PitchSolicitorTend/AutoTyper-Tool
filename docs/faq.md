# Extended FAQ — AutoTyper Tool

This page expands on the FAQ in the main [README.md](../README.md#frequently-asked-questions) with additional questions and troubleshooting tips for **AutoTyper Tool**, the free auto typer and keyboard automation software for Windows.

## Table of Contents

- [General](#general)
- [Download & Installation](#download--installation)
- [Usage](#usage)
- [Compatibility](#compatibility)
- [Privacy & Safety](#privacy--safety)
- [Project & Licensing](#project--licensing)

---

## General

### What does "AutoTyper" mean?
An **autotyper** (or "auto typer") is a program that automatically types text on your behalf by simulating keyboard key presses, instead of you typing manually. It's commonly used for automation, testing, accessibility, and productivity.

### What can I use AutoTyper Tool for?
Common uses include automatically typing repetitive messages, filling out forms, entering test data for QA, typing scripts for live demos/recordings, and assisting users who find manual typing difficult.

### Does AutoTyper Tool work offline?
Yes. AutoTyper Tool requires no internet connection and makes no network requests of any kind.

---

## Download & Installation

### Where can I download AutoTyper Tool?
The official download is the [AutoTyper.zip release on GitHub](https://github.com/PitchSolicitorTend/AutoTyper-Tool/releases/download/AutoTyper/AutoTyper.zip). Avoid downloading "AutoTyper Tool" from third-party sites, as they may bundle adware.

### Do I need to install anything?
No. AutoTyper Tool is a **portable application** — extract the ZIP and run `AutoTyper.exe` directly. Nothing is written to the Windows Registry.

### Does AutoTyper Tool work on Windows 7 or 8?
AutoTyper Tool officially supports **Windows 10 and Windows 11**. It may run on older versions but is not tested or supported there.

### Can I run AutoTyper Tool from a USB drive?
Yes — since it's portable and doesn't write configuration to the system by default, you can run it from a USB stick on multiple computers.

---

## Usage

### How do I make AutoTyper Tool type into a specific window?
Click into the target window/text field first so it has keyboard focus, then press the **start hotkey** (`F6` by default). AutoTyper Tool's **Start Delay** setting gives you a few seconds to switch windows after pressing the hotkey.

### Can I schedule AutoTyper Tool to run at a specific time?
Not natively yet — but you can combine AutoTyper Tool with the Windows Task Scheduler to launch it at a specific time, then use the start hotkey (or autostart settings) to begin typing.

### How do I type the same text multiple times automatically?
Enable **Loop / Repeat Mode** in Settings and choose either a fixed number of repetitions or "Infinite" (stop manually with `Esc`).

### Can I type from multiple text snippets in sequence?
Yes — save each snippet as a separate **preset** (see [Usage Guide → Presets](usage-guide.md#presets)) and load them one after another.

### How do I stop AutoTyper Tool in an emergency?
Press **`Esc`** at any time. This is a global hotkey and works even if AutoTyper Tool's window isn't focused.

---

## Compatibility

### Does AutoTyper Tool work with Discord, Slack, or other chat apps?
Yes. Since it simulates real keyboard input, it works with any application that accepts keyboard typing. For chat apps where `Enter` sends a message, set **New-Line Handling** to `Shift+Enter` so multi-line text isn't sent prematurely.

### Does AutoTyper Tool work in games?
It can type into most games' chat boxes or text fields the same way it works in any other application. However, games using kernel-level anti-cheat software may block simulated input entirely, or detecting automated input may violate the game's Terms of Service — see [Safety, Privacy and Responsible Use](../README.md#safety-privacy-and-responsible-use).

### Does AutoTyper Tool support multiple monitors?
Yes — AutoTyper Tool types into whichever window currently has keyboard focus, regardless of which monitor it's on.

### Does AutoTyper Tool support non-English keyboards/layouts?
Yes, AutoTyper Tool uses Unicode-based input simulation, which supports accented characters and many non-Latin scripts. Behavior can vary slightly depending on the target application's own input handling.

---

## Privacy & Safety

### Does AutoTyper Tool collect any data?
No. AutoTyper Tool does not collect, log, or transmit any data — including the text you type, your usage patterns, or system information. There is no analytics SDK and no network code.

### Is AutoTyper Tool open source?
Yes, the full source is available in this repository under the [MIT License](../LICENSE). You're free to audit, modify, and redistribute it.

### Why does my antivirus say AutoTyper Tool is a "PUA" or "RiskWare"?
This is a known false-positive pattern for the entire category of auto typer/auto clicker tools, because they use the same Windows input-simulation APIs as some malware. See [Installation Guide → Antivirus False Positives](installation.md#antivirus-false-positives) for details and how to verify the file is safe.

---

## Project & Licensing

### Can I use AutoTyper Tool commercially?
Yes. The MIT License permits commercial use, modification, and redistribution, provided the original copyright and license notice are included.

### How do I report a bug or request a feature?
Open an issue on the [Issues page](https://github.com/PitchSolicitorTend/AutoTyper-Tool/issues). See [CONTRIBUTING.md](../CONTRIBUTING.md) for guidelines.

### How do I report a security vulnerability?
See [SECURITY.md](../SECURITY.md) for our responsible-disclosure process — please do not post security issues publicly.

---

Still have questions? [Open an issue](https://github.com/PitchSolicitorTend/AutoTyper-Tool/issues) or check the [Usage Guide](usage-guide.md).
