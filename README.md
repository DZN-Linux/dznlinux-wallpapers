# DZN Linux Wallpapers

Official wallpaper collection for DZN Linux distribution.

## Overview

A curated collection of 115 high-quality wallpapers optimized for use with Arch Linux desktop environments, featuring themes ranging from nature photography to cyberpunk aesthetics.

**Version:** 1.0.0

## Contents

- **115 wallpapers** in JPG and PNG formats
- **Resolutions:** 1366x768 to 6016x4016 pixels
  - Full HD (1920x1080)
  - QHD (2560x1440)
  - 4K (3840x2160)
  - 5K+ (5000x3535 and higher)
  - Ultrawide formats
- **Total size:** ~152MB
- **Themes:** Nature, space, abstract, cyberpunk, technology, Arch Linux branded

## Installation

### From DZN Linux Repository (Recommended)

First, add the DZN Linux repository to your system:

```bash
# Add the PGP key
sudo pacman-key --recv-key BB31837564255477
sudo pacman-key --lsign-key BB31837564255477
```

Add the following to `/etc/pacman.conf`:

```ini
[dznlinux_repo]
SigLevel = Required DatabaseOptional
Server = https://repo.dozzen.me/archlinux/$repo/$arch

[dznlinux_repo_3party]
SigLevel = Required DatabaseOptional
Server = https://repo.dozzen.me/archlinux/$repo/$arch
```

Then install the package:

```bash
sudo pacman -Sy
sudo pacman -S dznlinux-wallpapers-git
```

### Manual Installation

```bash
# Clone repository
git clone https://github.com/DZN-Linux/dznlinux-wallpapers.git
cd dznlinux-wallpapers

# Copy wallpapers to system directories
sudo cp -r usr/share/backgrounds/dznlinux /usr/share/backgrounds/
sudo cp -r usr/share/wallpapers/DZNLinux /usr/share/wallpapers/
```

### From PKGBUILD

```bash
# Clone the PKGBUILD repository
git clone https://github.com/DZN-Linux/PKGBUILD.git
cd PKGBUILD/dznlinux-wallpapers

# Build and install
makepkg -si
```

## Usage

### KDE Plasma

Wallpapers are automatically available in the KDE wallpaper picker:

1. Right-click desktop → **Configure Desktop and Wallpaper**
2. Click **Get New Wallpapers** or browse to `/usr/share/backgrounds/dznlinux/`
3. Select any wallpaper to apply

The wallpapers are also available through KDE's native wallpaper browser via the metadata in `/usr/share/wallpapers/DZNLinux/`.

### Hyprland

#### Using hyprpaper

Add to `~/.config/hypr/hyprpaper.conf`:

```conf
preload = /usr/share/backgrounds/dznlinux/default.jpg
wallpaper = ,/usr/share/backgrounds/dznlinux/default.jpg
```

Or set a specific wallpaper:

```conf
preload = /usr/share/backgrounds/dznlinux/landscape-abstract-neon.jpg
wallpaper = ,/usr/share/backgrounds/dznlinux/landscape-abstract-neon.jpg
```

#### Using swaybg

```bash
swaybg -i /usr/share/backgrounds/dznlinux/default.jpg &
```

#### Using swww

```bash
swww img /usr/share/backgrounds/dznlinux/default.jpg
```

### Other Desktop Environments

Wallpapers are installed to the standard location `/usr/share/backgrounds/dznlinux/` and can be accessed by:

- **GNOME**: Settings → Background → Add Picture
- **XFCE**: Desktop Settings → Background → Folder: `/usr/share/backgrounds/dznlinux/`
- **i3/sway**: Using `feh`, `nitrogen`, or `swaybg`
- **Any WM**: Use your preferred wallpaper manager

## File Structure

```
usr/
└── share/
    ├── backgrounds/
    │   └── dznlinux/          # All wallpaper files
    │       ├── default.jpg    # Default wallpaper
    │       ├── nature.jpg
    │       ├── arch-linux-wallpaper-*.jpg
    │       └── ...
    └── wallpapers/
        └── DZNLinux/          # KDE Plasma metadata
            └── metadata.desktop
```

## Wallpaper Categories

- **Nature**: Landscapes, mountains, forests, lakes (20+ images)
- **Space**: Planets, galaxies, astronomy (15+ images)
- **Abstract**: Geometric, liquid, fractal art (25+ images)
- **Cyberpunk/Neon**: Futuristic city scenes, neon aesthetics (15+ images)
- **Technology**: Tech-inspired abstract designs (10+ images)
- **Arch Linux Branded**: Official Arch Linux wallpapers (20+ images)
- **Minimalist**: Clean, simple designs (10+ images)

## Featured Wallpapers

- `default.jpg` - Default DZN Linux wallpaper (2560x1440)
- `arch-linux-wallpaper-*` - Official Arch Linux collection
- `landscape-abstract-neon.jpg` - Neon landscape (3840x2160)
- `northern-night.jpg` - Aurora borealis (3840x2160)
- `yosemite-sunset-3840x2160.jpg` - Yosemite landscape (4K)
- `astronaut_jellyfish.jpg` - Surreal space art (3840x2160)

## Building from Source

This repository is the source for the `dznlinux-wallpapers-git` Arch package.

### Prerequisites

```bash
sudo pacman -S base-devel git
```

### Build Instructions

See the [PKGBUILD repository](https://github.com/DZN-Linux/PKGBUILD/tree/main/dznlinux-wallpapers) for complete build instructions.

## Versioning

This project uses [Semantic Versioning](https://semver.org/):

- **MAJOR**: Breaking changes to file paths or structure
- **MINOR**: New wallpapers added
- **PATCH**: Bug fixes, metadata updates

Current version is tracked in the `VERSION` file.

## Contributing

### Adding New Wallpapers

1. **Image requirements:**
   - Format: JPG or PNG
   - Minimum resolution: 1920x1080
   - Recommended: 3840x2160 (4K) or higher
   - File size: Keep under 5MB per image (optimize if needed)

2. **Add to repository:**
   ```bash
   cp your-wallpaper.jpg usr/share/backgrounds/dznlinux/
   ```

3. **Test installation:**
   ```bash
   sudo cp usr/share/backgrounds/dznlinux/your-wallpaper.jpg \
        /usr/share/backgrounds/dznlinux/
   ```

4. **Submit pull request:**
   - Include description of image
   - Credit original source if applicable
   - Ensure license is compatible (GPL/CC0/Public Domain)

### License Requirements

Only wallpapers that are GPL-compatible, Creative Commons (CC0, CC-BY), or Public Domain should be submitted. Please verify licensing before submitting.

## Credits

- **Curated by:** DZN Linux Team
- **Some images from:**
  - Arch Linux official wallpapers
  - GNOME Adwaita wallpapers
  - Various GPL/CC0 sources

Full attribution for individual images available upon request.

## License

This collection is licensed under the **GNU General Public License v3.0** (GPL-3.0).

See [LICENSE](LICENSE) file for full license text.

Individual images may have additional attribution requirements - see credits section.

## Links

- **Source Repository:** https://github.com/DZN-Linux/dznlinux-wallpapers
- **PKGBUILD Repository:** https://github.com/DZN-Linux/PKGBUILD
- **DZN Linux:** https://github.com/DZN-Linux
- **Issues:** https://github.com/DZN-Linux/dznlinux-wallpapers/issues

## Support

For issues, questions, or suggestions:

- Open an issue: https://github.com/DZN-Linux/dznlinux-wallpapers/issues
- Contact: dznlinux@gmail.com

## Changelog

### Version 1.0.0 (2024-12-10)

- Initial release
- 115 curated wallpapers
- Support for KDE Plasma and Hyprland
- Multiple resolutions from 1080p to 5K+
- Organized in standard FHS paths
