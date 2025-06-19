# Desktop Application Releases

This repository contains the official releases for our Kotlin Multiplatform Desktop application.

## Download Links

### Latest Release
- **Linux (DEB)**: [desktop-latest.deb](https://github.com/YOUR_USERNAME/YOUR_PUBLIC_REPO/releases/latest/download/desktop-latest.deb)
- **Windows (MSI)**: [desktop-latest.msi](https://github.com/YOUR_USERNAME/YOUR_PUBLIC_REPO/releases/latest/download/desktop-latest.msi)
- **Windows (EXE)**: [desktop-latest.exe](https://github.com/YOUR_USERNAME/YOUR_PUBLIC_REPO/releases/latest/download/desktop-latest.exe)
- **macOS (DMG)**: [desktop-latest.dmg](https://github.com/YOUR_USERNAME/YOUR_PUBLIC_REPO/releases/latest/download/desktop-latest.dmg)

### Release Information
The latest release information is available in JSON format: [latest-release.json](https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_PUBLIC_REPO/main/latest-release.json)

## File Structure

### Release Files
Each release includes both versioned and latest files:
- `desktop-{version}.deb` - Linux DEB package (specific version)
- `desktop-latest.deb` - Linux DEB package (always latest)
- `desktop-{version}.msi` - Windows MSI installer (specific version)
- `desktop-latest.msi` - Windows MSI installer (always latest)
- `desktop-{version}.exe` - Windows portable executable (specific version)
- `desktop-latest.exe` - Windows portable executable (always latest)
- `desktop-{version}.dmg` - macOS DMG installer (specific version)
- `desktop-latest.dmg` - macOS DMG installer (always latest)

### Metadata Files
- `latest-release.json` - Information about the current latest release
- `version-history.json` - Complete history of all releases
- `releases/` - Directory containing all release files

## API Usage

### Get Latest Release Info
```bash
curl https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_PUBLIC_REPO/main/latest-release.json
```

Example response:
```json
{
  "version": "1.2.3",
  "release_date": "2025-06-20T10:30:00Z",
  "commit_sha": "abc123...",
  "files": {
    "linux": {
      "deb": "desktop-1.2.3.deb",
      "latest_deb": "desktop-latest.deb"
    },
    "windows": {
      "msi": "desktop-1.2.3.msi",
      "latest_msi": "desktop-latest.msi",
      "exe": "desktop-1.2.3.exe",
      "latest_exe": "desktop-latest.exe"
    },
    "macos": {
      "dmg": "desktop-1.2.3.dmg",
      "latest_dmg": "desktop-latest.dmg"
    }
  },
  "download_urls": {
    "linux": {
      "deb": "https://github.com/YOUR_USERNAME/YOUR_PUBLIC_REPO/releases/latest/download/desktop-latest.deb"
    },
    "windows": {
      "msi": "https://github.com/YOUR_USERNAME/YOUR_PUBLIC_REPO/releases/latest/download/desktop-latest.msi",
      "exe": "https://github.com/YOUR_USERNAME/YOUR_PUBLIC_REPO/releases/latest/download/desktop-latest.exe"
    },
    "macos": {
      "dmg": "https://github.com/YOUR_USERNAME/YOUR_PUBLIC_REPO/releases/latest/download/desktop-latest.dmg"
    }
  }
}
```

### Get Version History
```bash
curl https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_PUBLIC_REPO/main/version-history.json
```

## Installation Instructions

### Linux
```bash
# Download and extract
wget https://github.com/YOUR_USERNAME/YOUR_PUBLIC_REPO/releases/latest/download/desktop-linux-latest.tar.gz
tar -xzf desktop-linux-latest.tar.gz

# Install (if .deb package is included)
sudo dpkg -i *.deb
```

### Windows
1. Download: [desktop-windows-latest.zip](https://github.com/YOUR_USERNAME/YOUR_PUBLIC_REPO/releases/latest/download/desktop-windows-latest.zip)
2. Extract the ZIP file
3. Run the installer (.msi) or executable (.exe)

### macOS
```bash
# Download and extract
curl -L https://github.com/YOUR_USERNAME/YOUR_PUBLIC_REPO/releases/latest/download/desktop-macos-latest.tar.gz -o desktop-macos-latest.tar.gz
tar -xzf desktop-macos-latest.tar.gz

# Install the .dmg file
open *.dmg
```

## Auto-Update Integration

For applications with auto-update functionality, use these endpoints:

- **Version Check**: `https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_PUBLIC_REPO/main/latest-release.json`
- **Download Latest**: Use the `download_urls` from the JSON response

## Release Process

Releases are automatically built and published from our private repository using GitHub Actions. Each release includes:

1. **Cross-platform builds** for Linux, Windows, and macOS
2. **Versioned archives** for historical access
3. **Latest archives** with stable URLs for easy linking
4. **Metadata files** for programmatic access
5. **GitHub Releases** with all assets attached

## Support

For issues, bug reports, or feature requests, please visit our main project repository or contact us through our official channels.

---

*This repository is automatically maintained. Do not make manual changes to release files.*
