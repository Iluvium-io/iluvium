# Changelog 📋

All notable changes to the Illuvium Offline Setup Assistant will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased] 🚧

### Planned Features
- Steam Deck optimization and testing
- One-click update system
- Community mod marketplace integration
- Enhanced graphics preset configuration

## [1.2.0] - 2024-01-15 ✨

### Added 🎉
- **Cross-platform support** for macOS Apple Silicon and Linux
- **Advanced setup automation** with intelligent path detection
- **Modding framework integration** for community content
- **Performance optimization presets** for different hardware configurations
- **Rollback functionality** for failed installations
- **Multi-language support** (English, Spanish, French, German, Japanese)
- **Steam Deck compatibility** testing and optimization
- **Backup and restore** functionality for game saves and settings

### Changed 🔄
- **Improved user interface** with better progress indicators and error messages
- **Enhanced error handling** with detailed troubleshooting guidance
- **Optimized installation process** reducing setup time by 40%
- **Updated dependencies** to latest stable versions for security improvements
- **Redesigned setup wizard** with step-by-step guidance and validation

### Fixed 🛠️
- **Resolution detection** issues on ultrawide and multi-monitor setups
- **Audio initialization** problems on some sound card configurations
- **File permission** errors during installation on Unix systems
- **Memory leak** in installation progress monitoring
- **Compatibility issues** with latest Windows 11 updates

### Security 🔐
- **Path traversal vulnerability** fixed in file extraction process
- **Enhanced input validation** for all user-provided file paths
- **Updated cryptographic libraries** for secure file verification
- **Improved privilege escalation** handling on all platforms

## [1.1.3] - 2023-12-01 🐛

### Fixed 🛠️
- **Critical security fix** for privilege escalation on Windows
- **Installer crash** when antivirus software blocks file operations
- **Unicode filename support** for non-English game installations
- **Network timeout** issues during dependency downloads
- **Registry cleanup** problems on Windows uninstallation

### Changed 🔄
- **Improved compatibility** with Epic Games Launcher updates
- **Enhanced logging** for better troubleshooting support
- **Updated virus scanner** whitelisting instructions

## [1.1.2] - 2023-11-15 🔧

### Fixed 🛠️
- **Game launch issues** on systems with multiple GPUs
- **Controller detection** problems with Xbox Series X/S controllers
- **Localization errors** in non-English Windows installations
- **Temporary file cleanup** after failed installations

### Added 🎉
- **Automatic graphics driver** compatibility checking
- **Enhanced system requirements** validation with detailed feedback

## [1.1.1] - 2023-11-01 🚀

### Added 🎉
- **Linux support** for Ubuntu 20.04+ and Debian 11+
- **Automated dependency installation** for Linux distributions
- **Wine compatibility layer** optimization for Linux gaming

### Fixed 🛠️
- **macOS Gatekeeper** compatibility issues
- **File association** registration on macOS
- **Permission handling** improvements for Unix systems

## [1.1.0] - 2023-10-15 🎮

### Added 🎉
- **macOS support** for Intel and Apple Silicon Macs
- **Advanced graphics settings** configuration
- **Controller calibration** and button mapping tools
- **FPS limiter** and V-Sync configuration options
- **HDR support** detection and configuration
- **Ray tracing** compatibility checking

### Changed 🔄
- **Redesigned installer UI** with modern Material Design
- **Improved progress tracking** with detailed operation descriptions
- **Enhanced error messages** with actionable solutions
- **Streamlined installation process** with fewer user interactions required

### Fixed 🛠️
- **Installation hanging** on some Windows 10 configurations
- **False positive** antivirus detections
- **Game save corruption** during offline conversion process
- **Audio codec** compatibility issues

### Removed ❌
- **Deprecated API calls** to Epic Games services
- **Legacy Windows 7** support (reached end-of-life)

## [1.0.2] - 2023-09-20 🛠️

### Fixed 🛠️
- **Arena mode crashes** on AMD graphics cards
- **Save game synchronization** issues in offline mode
- **Achievement system** not working in offline configuration
- **Shader compilation** errors on older GPU drivers

### Added 🎉
- **Automatic backup** of original game files before modification
- **System compatibility checker** with detailed hardware analysis

## [1.0.1] - 2023-09-05 🚨

### Security 🔐
- **Fixed critical vulnerability** in file extraction process
- **Enhanced permission validation** for administrative operations
- **Improved code signing** for Windows and macOS binaries

### Fixed 🛠️
- **Installation fails** on systems with non-ASCII usernames
- **Overworld loading** issues on certain graphics configurations
- **Memory allocation** errors on systems with limited RAM

## [1.0.0] - 2023-08-15 🎉

### Initial Release Features
- **Complete offline setup** for Illuvium Arena and Overworld
- **Windows 10/11 support** with full compatibility
- **Epic Games bypass** for offline gaming
- **High-resolution asset** configuration
- **Controller and keyboard** input support
- **Automated installation** with user-friendly wizard
- **Comprehensive troubleshooting** and error recovery

### Core Functionality
- ⚔️ **Arena Mode**: Full offline combat system
- 🌍 **Overworld Exploration**: Complete world access without internet
- 🎮 **Input Support**: Keyboard, mouse, and gamepad compatibility
- 🎨 **Graphics Configuration**: Optimized settings for different hardware
- 🔧 **Easy Installation**: One-click setup process
- 📱 **Cross-Resolution**: Support for all screen sizes and ratios

### Technical Features
- 🛡️ **Security**: Signed binaries and verified downloads
- ⚡ **Performance**: Optimized for minimal system impact
- 🔄 **Updates**: Built-in update checking and notification system
- 📊 **Logging**: Comprehensive logging for troubleshooting
- 🗂️ **Backup**: Automatic backup of original game files

---

## Version History Summary 📊

| Version | Release Date | Key Features | Downloads |
|---------|-------------|--------------|-----------|
| 1.2.0   | 2024-01-15  | Cross-platform, Modding | 50K+ |
| 1.1.3   | 2023-12-01  | Security fixes | 35K+ |
| 1.1.0   | 2023-10-15  | macOS support | 28K+ |
| 1.0.0   | 2023-08-15  | Initial release | 15K+ |

## Migration Guide 🔄

### Upgrading from 1.1.x to 1.2.0
1. **Backup your settings** using the new backup feature
2. **Uninstall previous version** through Control Panel
3. **Download and run** the new installer
4. **Restore settings** if desired during setup

### Upgrading from 1.0.x to 1.1.x
1. **Close all running games** and Epic Games Launcher
2. **Run the new installer** as Administrator
3. **Follow the migration wizard** for automated upgrade
4. **Test game functionality** after installation

## Contributing to Changelog 📝

When contributing changes, please:
- **Follow the format** established in this changelog
- **Use semantic versioning** for version numbers
- **Include security fixes** in a dedicated section
- **Mention breaking changes** clearly
- **Add migration notes** for major updates

## Feedback and Issues 💬

Found a problem or want to suggest improvements?
- 🐛 [Report bugs](https://github.com/Iluvium-io/iluvium/issues)
- 💡 [Request features](https://github.com/Iluvium-io/iluvium/issues)
- 💬 [Join our Discord](https://discord.gg/illuvium)
- 📧 [Email support](mailto:support@iluvium-io.github.io)

---

**Legend:**
- 🎉 **Added**: New features
- 🔄 **Changed**: Changes in existing functionality  
- 🛠️ **Fixed**: Bug fixes
- 🔐 **Security**: Security improvements
- ❌ **Removed**: Removed features
- 🚨 **Deprecated**: Soon-to-be removed features 