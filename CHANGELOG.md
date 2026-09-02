# Changelog

## [1.0.6] - 2026-09-02

### Changed

- Kept only the option names **Enable typewriter sound** and **Enable braille writer sound**, with their standard checked or unchecked states.
- Removed the additional accessible descriptions, on/off announcements, and redundant Help explanations for the two sound options.
- Updated application, installer, documentation, and release artifacts to version 1.0.6.

## [1.0.5] - 2026-09-02

### Changed

- Renamed the two Edit-menu commands to **Enable typewriter sound** and **Enable braille writer sound**.
- Made the typewriter and Perkins Brailler sounds fully independent checkable options. Either sound, both sounds, or neither sound can now be enabled.
- When both options are checked, WriterBook plays a combined sample so both mechanical sounds remain audible.
- Migrated the saved Perkins selection from version 1.0.4 to the new independent braille-sound setting.
- Updated in-app Help, project documentation, installer metadata, and release artifacts for version 1.0.5.

## [1.0.4] - 2026-09-02

### Added

- Added two persistent, checkable commands to **Edit**: **Enable typewriter sound** and **Use braille writer sound**.
- Added embedded old-typewriter and classic Perkins Brailler keystroke sounds for typing, deleting, pasting, undoing, and other text edits.
- Added `F7`, `F8`, `F9`, and `F10` to the visible and screen-reader-accessible names of the bookmark commands in **Edit**.

### Fixed

- `F7` and `F8` bookmark confirmations are now announced from the focused writing area, so NVDA, JAWS, and other screen readers can reliably read them.
- Repeated announcements no longer restore a stale announcement as the writing area's accessible name.

### Changed

- Updated application, installer, update-check, file metadata, documentation, and release artifact names to version 1.0.4.
- Added third-party audio attribution and license notices to portable and installed distributions.
