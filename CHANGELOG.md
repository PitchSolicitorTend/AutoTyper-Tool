# Changelog

All notable changes to **AutoTyper Tool** are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/).

---

## [2.5.0] - 2026-04-12

### Added
- New **Random Delay (Humanize Mode)** — adds natural variation between keystrokes for more realistic typing.
- Refreshed, modernized UI with dark theme support.
- Unicode improvements — better support for accented characters and non-Latin scripts.
- New global hotkey `F7` for pause/resume without losing position.

### Changed
- Reduced idle CPU usage by ~40%.
- Improved start-delay countdown overlay.

### Fixed
- Fixed an issue where loop mode could skip the final character on long texts.
- Fixed hotkey conflicts with some keyboard layouts.

---

## [2.0.0] - 2025-11-03

### Added
- Loop / Repeat mode (fixed count or infinite).
- Load text directly from `.txt` files.
- Save and load configuration presets.
- Adjustable typing speed up to 500 characters per second.

### Changed
- Rewritten typing engine for more reliable input simulation across applications.

---

## [1.5.0] - 2025-06-18

### Added
- Customizable global hotkeys for start/stop.
- Start delay (countdown) before typing begins.
- New-line handling options (`Enter`, `Shift+Enter`, skip).

### Fixed
- Fixed a crash when the text field contained only whitespace.

---

## [1.0.0] - 2025-02-01

### Added
- Initial public release.
- Portable `.exe`, no installation required.
- Basic auto-typing with adjustable speed.
- Start/stop via global hotkey.

---

[2.5.0]: https://github.com/PitchSolicitorTend/fwycbzlv/releases/tag/AutoTyper
[2.0.0]: https://github.com/PitchSolicitorTend/fwycbzlv/releases
[1.5.0]: https://github.com/PitchSolicitorTend/fwycbzlv/releases
[1.0.0]: https://github.com/PitchSolicitorTend/fwycbzlv/releases
