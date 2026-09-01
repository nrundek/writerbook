# WriterBook

WriterBook is a simple, accessible digital notebook for Windows. It provides a distraction-free writing page, keyboard-first navigation, screen-reader-friendly controls, live text counters, writing goals, persistent bookmarks, and export to Microsoft Word or PDF.

The application is available in Croatian, Serbian, and English. The installer is entirely in English.

## Features

- Native Windows rich-text editor
- Accessible menus and status information for screen readers
- Full keyboard operation
- Live word, character, character-with-spaces, and line counters
- Writing goals with a progress bar
- Persistent bookmarks stored inside the `.writer` notebook
- Export to Microsoft Word (`.docx`) or PDF (`.pdf`)
- Croatian, Serbian, and English interface languages
- Windows High Contrast support
- Built-in GitHub update check
- Portable application and installer editions

## Keyboard shortcuts

| Shortcut | Action |
| --- | --- |
| `F1` | Open Help |
| `F2` | Announce the word count |
| `F3` | Announce characters excluding spaces |
| `F4` | Announce characters including spaces |
| `F5` | Announce the line count |
| `F6` | Set a writing goal and show progress |
| `F7` | Add a bookmark or resume from a saved bookmark |
| `Ctrl+N` | Create a new notebook |
| `Ctrl+O` | Open a WriterBook notebook |
| `Ctrl+S` | Save the notebook |
| `Ctrl+Shift+S` | Export to Microsoft Word or PDF |
| `Ctrl+F` | Find text |
| `Ctrl+H` | Find and replace text |
| `Ctrl+Z` | Undo |
| `Ctrl+X` | Cut |
| `Ctrl+C` | Copy |
| `Ctrl+V` | Paste plain text |
| `Ctrl+A` | Select all |
| `Alt+F4` | Close WriterBook |

The F2–F5 commands announce their values without opening a dialog that must be closed.

## Writing goals

Press `F6` or open **Counts > Writing goal and progress bar**. Choose one of the following goal types:

- words
- characters excluding spaces
- characters including spaces

Enter a positive whole number. The current value, target, percentage, and progress bar are then shown in the status bar.

## Bookmarks

Press `F7` at the position where you stop writing for the day. The bookmark is saved inside the `.writer` notebook.

After reopening a notebook, press `F7` to return to its saved bookmark. If the notebook contains several bookmarks, WriterBook presents an accessible list. Commands for adding, opening, and deleting bookmarks are also available from the **Edit** menu.

Bookmarks automatically follow their positions when text is inserted or removed before them.

## Languages

Open **Help > Language** and select:

- Hrvatski
- Srpski
- English

The selected language is applied to the entire application immediately and is remembered for the next launch. The setup program remains in English and lets the user choose the application's initial language.

## Installation

Download `WriterBook-1.0-Setup.exe` from the latest GitHub release and run it. Administrator permission is required because WriterBook is installed for all Windows users.

The installer:

- installs WriterBook in `C:\Program Files\WriterBook` by default
- creates Start menu shortcuts
- optionally creates a desktop shortcut
- associates `.writer` files with WriterBook
- preserves user notebooks and exported documents during upgrades or removal

For a portable installation, download and run `WriterBook.exe`.

## Updates

Use **Help > Check for updates** to check the latest release from [`nrundek/writerbook`](https://github.com/nrundek/writerbook/releases/latest).

If the installed version is current, WriterBook reports that no update is available. When a newer release exists, a download command appears in the Help menu. WriterBook prefers a release asset whose filename ends in `Setup.exe`; otherwise, it opens the release page.

Release tags should contain a version number, for example:

```text
v1.0.0
v1.1.0
v2.0.0
```

## Building from source

WriterBook is a native Windows Forms application written in C#. It is built with the .NET Framework compiler included with Windows.

From PowerShell in the repository root, run:

```powershell
.\writer-build\build.ps1
```

The build creates:

```text
writer-dist\WriterBook.exe
writer-dist\WriterBook-1.0-Setup.exe
```

The build script also embeds the portable application in the installer.

## Testing

WriterBook includes automated checks for:

- `.writer` notebook saving and loading
- Microsoft Word and PDF export
- persistent bookmarks
- text counters and writing-goal progress
- GitHub release parsing
- accessible menus and control names
- installer output and accessibility

Formal accessibility verification should also include manual testing with NVDA or JAWS on the target Windows versions.

## Data and privacy

WriterBook stores application settings in the user's Windows application-data folder and stores notebook content in files chosen by the user. The application only accesses the internet when the user explicitly runs **Check for updates**.

## License

No license has been specified yet. Add a `LICENSE` file before inviting third-party contributions or redistribution.
