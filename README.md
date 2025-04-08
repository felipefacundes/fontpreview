# Font Preview ✨

[![License: GPLv3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Version](https://img.shields.io/badge/Version-1.0-green)](https://github.com/felipefacundes/fontpreview)
[![Shell](https://img.shields.io/badge/Shell-Bash-lightgrey)](https://www.gnu.org/software/bash/)

A lightning-fast, terminal-based font previewer with Sixel graphics support, designed for designers and developers who work with fonts in Linux/Unix environments.

![Demo Animation](demo.gif)

## Features 🌟

- 🖼️ **Interactive previews** with real-time rendering
- 🎨 **Fully customizable** colors, sizes, and sample text
- 📋 **Automatic clipboard** integration (supports X11, Wayland, Termux)
- 🔍 **Fuzzy search** through all available system fonts
- 🖌️ **Image export** capability for documentation
- 📱 **Termux/Android** compatible
- 🎚️ **Environment variable** configuration
- 🌈 **Sixel graphics** support for modern terminals

## Installation 📦

### Prerequisites
```bash
# Debian/Ubuntu
sudo apt install imagemagick fzf

# Arch Linux
sudo pacman -S imagemagick fzf

# Fedora
sudo dnf install ImageMagick fzf

# macOS (via Homebrew)
brew install imagemagick fzf
```

### Install Script
```bash
wget https://raw.githubusercontent.com/felipefacundes/fontpreview/main/fontpreview -O ~/.local/bin/fontpreview
chmod +x ~/.local/bin/fontpreview
```

## Usage 🚀

### Basic Interactive Mode
```bash
fontpreview
```

### Custom Preview Settings
```bash
fontpreview --margin-height 90 --size "1200x800" --font-size 36 --bg-color "#290a04" --fg-color "#f5e0c9"
```

### Export to Image
```bash
fontpreview -i "FiraCode.otf" -o "fira_preview.png"
```

### Show Help
```bash
fontpreview --help
```

## Configuration ⚙️

Customize defaults through environment variables (add to your `.bashrc`/`.zshrc`):

```bash
export FONT_SIZE=36
export SIZE="1200x800"
export BG_COLOR="#290a04"
export FG_COLOR="#f5e0c9"
export PREVIEW_TEXT="Custom Preview Text\n1234567890\nABCDEFGHIJKLMNOPQRSTUVWXYZ"
export FZF_MARGIN_R=70  # Right margin percentage
export FZF_MARGIN_H=90  # Height percentage
```

## Keybindings ⌨️

While in interactive mode:
- `↑`/`↓` - Navigate font list
- `Enter` - Select font (copies to clipboard)
- `Esc`/`Ctrl+C` - Exit

## Supported Terminals 🖥️

For best experience, use a Sixel-compatible terminal:
- [WezTerm](https://wezfurlong.org/wezterm/)
- [Contour](https://github.com/contour-terminal/contour)
- [XTerm with VT340 emulation](https://invisible-island.net/xterm/)
- [Alacritty with Sixel patch](https://github.com/microo8/alacritty-sixel)

## Troubleshooting 🔧

**Problem:** Preview not displaying  
**Solution:** Ensure your terminal supports Sixel graphics or install `feh` as fallback:
```bash
sudo pacman -S feh  # ArchLinux
sudo apt install feh  # Debian/Ubuntu
```

**Problem:** Missing fonts  
**Solution:** Specify exact path with `-i` flag
**Install** To install additional fonts on your system, use the `--install` flag and provide the font file exact path with `-i`

## Contributing 🤝

Pull requests are welcome! For major changes, please open an issue first to discuss proposed changes.

## License 📜

This project is licensed under the GPLv3 License - see the [LICENSE](LICENSE) file for details.

---

Crafted with ❤️ by [Felipe Facundes]