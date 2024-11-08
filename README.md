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
git clone https://github.com/LightNabz/dotfiles.git
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

### 3. Install GNOME Extensions
To install GNOME Shell extensions, you can loop through gnome-extensions.txt:
```bash
while IFS= read -r extension; do
    gnome-extensions install "$extension"
done < gnome-extensions.txt
```

### 4. Restore GNOME Terminal Profiles
```bash
dconf load /org/gnome/terminal/legacy/profiles:/ < gnome-terminal-profiles.dconf
```

### 5. Copy Themes, Icons, and Configurations
```bash
cp -r .themes ~/
cp -r .icons ~/
cp -r .config/gtk-3.0 ~/.config/
cp -r .config/gtk-4.0 ~/.config/
cp -r .config/gnome-shell ~/.config/
```
