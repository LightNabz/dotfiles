l# GNOME Dotfiles

This repository contains my GNOME desktop configuration files.

## Contents

- **gnome-settings.dconf**: Contains all GNOME desktop settings exported from `dconf`.
- **gnome-extensions.txt**: List of GNOME Shell extensions.
- **gnome-terminal-profiles.dconf**: Configuration for GNOME Terminal profiles.
- **themes/**: Catppuccin Frappe Blue.
- **icons/**: ePapyrus-Dark icons.
- **config/**: Configuration files for GTK3, GTK4, and GNOME Shell.

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/gnome-dotfiles.git
cd gnome-dotfiles
```

### 2. Restore GNOME Settings

```bash
dconf load / < gnome-settings.dconf
```

### 3. Export GNOME Shell Extensions

```bash
gnome-extensions list > gnome-extensions.txt
```

### 4. Copy/Move themes, icons, and fonts to,
themes to ~/.themes Or /usr/share/themes
icons to ~/.icons Or /usr/share/icons
fonts to ~/.fonts Or /usr/share/fonts

### 5. Copy/Move key configuration files to,
```bash
~/.config/gtk-4.0/
```
