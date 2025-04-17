# 🧾 Nano — Simple and Friendly Terminal Text Editor

`nano` is a beginner-friendly, lightweight terminal-based text editor. It’s often the default editor on many Linux systems and is perfect for quick edits in the terminal.

---

## ✅ Features

- Easy-to-use interface with on-screen shortcuts
- No modes (unlike Vim)
- Supports syntax highlighting
- Undo/redo functionality
- Search and replace
- Lightweight and fast

---

## 🔧 Installation

### Debian/Ubuntu:
```bash
sudo apt update && sudo apt install nano
```

### Arch Linux:
```bash
sudo pacman -S nano
```

### macOS (via Homebrew):
```bash
brew install nano
```

---

## 🚀 Opening Files

```bash
nano filename.txt
```

- If the file doesn't exist, `nano` will create it when you save.
- You can also open files with specific line numbers:
```bash
nano +15 filename.txt
```

---

## ⌨️ Basic Keybindings

Nano uses **Control (Ctrl)** key shortcuts. You’ll see many of them listed at the bottom of the screen while editing.

| Shortcut        | Action                          |
|-----------------|---------------------------------|
| `Ctrl+O`        | Save file ("Write Out")         |
| `Ctrl+X`        | Exit nano                       |
| `Ctrl+G`        | Help                            |
| `Ctrl+K`        | Cut current line (cut text)     |
| `Ctrl+U`        | Paste cut line (uncut text)     |
| `Ctrl+W`        | Search for text                 |
| `Ctrl+\`        | Search and replace              |
| `Ctrl+C`        | Show cursor position            |
| `Ctrl+_`        | Go to specific line and column  |
| `Alt+U`         | Undo                            |
| `Alt+E`         | Redo                            |

---

## 📝 Editing Tips

- Use arrow keys to navigate.
- Text automatically wraps unless disabled with `nano -w`.
- To select text, use `Ctrl+^` to mark the beginning, then move the cursor. The selection can be cut (`Ctrl+K`) or copied (`Alt+6`).

---

## 💡 Command-Line Options

| Option        | Description                            |
|---------------|----------------------------------------|
| `-w`          | Disable line wrapping                  |
| `-l`          | Enable line numbers                    |
| `-c`          | Show cursor position constantly        |
| `-m`          | Enable mouse support                   |
| `-i`          | Auto-indent new lines                  |

Example:
```bash
nano -c -l myfile.txt
```

---

## 🎨 Syntax Highlighting

Nano supports syntax highlighting via configuration.

Enable it in your config file:

```bash
nano ~/.nanorc
```

Include common syntax definitions (example):

```bash
include "/usr/share/nano/python.nanorc"
include "/usr/share/nano/html.nanorc"
include "/usr/share/nano/bash.nanorc"
```

You can find many enhanced `.nanorc` definitions here:
- [https://github.com/scopatz/nanorc](https://github.com/scopatz/nanorc)

---

## 🔐 sudo + nano

To edit system files:

```bash
sudo nano /etc/hosts
```

This gives root access to save protected files.

---

## 🔁 Search and Replace

### Search:
- `Ctrl+W`, then type your term and press `Enter`

### Replace:
- `Ctrl+\`, type the word to find, then replacement, press `Enter`

Nano will ask you for confirmation:
- Press `Y` to confirm, `A` to replace all, or `Ctrl+C` to cancel

---

## ⚙️ Configuration File (`~/.nanorc`)

You can tweak nano using your personal config file.

Example:
```bash
set linenumbers
set tabsize 4
set autoindent
set softwrap
```

---

## 📚 More Info

- Manual:  
```bash
man nano
```

- Official site: [https://nano-editor.org](https://nano-editor.org)

---

## 🧩 Alternatives

- `vim` — Powerful modal text editor
- `neovim` — Modern Vim fork
- `emacs` — Full-featured but complex text editor
