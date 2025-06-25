# Contributing to Illuvium Offline Setup Assistant 🎮

Thank you for your interest in contributing to the Illuvium Offline Setup Assistant! This document provides guidelines and information for contributors.

## 🌟 How to Contribute

We welcome contributions from the gaming community! Here are several ways you can help improve the project:

### 🐛 Bug Reports
- **Search existing issues** before creating a new one
- **Use the bug report template** when filing issues
- **Include system information** (OS, hardware specs, game version)
- **Provide step-by-step reproduction instructions**
- **Attach screenshots or videos** when helpful

### 💡 Feature Requests
- **Check existing feature requests** to avoid duplicates
- **Use the feature request template**
- **Explain the use case** and why it would benefit users
- **Consider implementation complexity** and maintenance burden

### 🔧 Code Contributions
- **Fork the repository** and create a feature branch
- **Follow coding standards** outlined below
- **Write clear commit messages** using conventional commits
- **Include tests** for new functionality
- **Update documentation** as needed

### 📝 Documentation
- **Improve setup guides** and troubleshooting sections
- **Add translation support** for different languages
- **Create video tutorials** for complex setup processes
- **Write blog posts** about advanced usage

### 🎨 Design & Assets
- **UI/UX improvements** for the setup assistant
- **Icon and branding assets** following project guidelines
- **Screenshot and media updates** for documentation
- **Community promotional materials**

## 🚀 Getting Started

### Prerequisites
- **Git** installed and configured
- **Node.js 16+** for build tools and development
- **Visual Studio Code** recommended IDE
- **Basic understanding** of gaming setup and offline installations

### Development Setup
```bash
# Clone your fork
git clone https://github.com/YOUR-USERNAME/iluvium.git
cd iluvium

# Install dependencies
npm install

# Set up development environment
npm run setup

# Run tests
npm test

# Start development server
npm run dev
```

### Building and Testing
```bash
# Run full test suite
npm run test:full

# Build for all platforms
npm run build:all

# Test installation on local system
npm run test:install
```

## 📋 Coding Standards

### General Guidelines
- **Use TypeScript** for type safety and better documentation
- **Follow ESLint configuration** for consistent code style
- **Write descriptive variable names** and function documentation
- **Keep functions small** and focused on single responsibilities
- **Use async/await** instead of promise chains

### Git Workflow
```bash
# Create feature branch
git checkout -b feature/your-feature-name

# Make changes and commit
git add .
git commit -m "feat: add offline validation for arena mode"

# Push and create PR
git push origin feature/your-feature-name
```

### Commit Message Format
We use [Conventional Commits](https://conventionalcommits.org/):

```
type(scope): short description

feat(installer): add support for macOS Apple Silicon
fix(launcher): resolve crash on Windows 11
docs(readme): update installation instructions
chore(deps): update security dependencies
```

## 🧪 Testing Guidelines

### Test Categories
- **Unit Tests**: Core functionality and utilities
- **Integration Tests**: Setup process end-to-end
- **Platform Tests**: Cross-platform compatibility
- **User Acceptance**: Real-world usage scenarios

### Writing Tests
```typescript
import { describe, it, expect } from 'vitest';
import { setupValidator } from '../src/validator';

describe('Setup Validator', () => {
  it('should validate system requirements', () => {
    const result = setupValidator.checkSystemRequirements();
    expect(result.isValid).toBe(true);
    expect(result.errors).toHaveLength(0);
  });
});
```

## 📖 Documentation Standards

### README Updates
- Keep installation instructions **up-to-date** with latest releases
- Add **troubleshooting sections** for common issues
- Include **platform-specific notes** when applicable
- Update **feature lists** when adding new functionality

### Code Documentation
```typescript
/**
 * Validates Illuvium installation and configures offline mode
 * @param installPath - Path to Illuvium game installation
 * @param options - Configuration options for offline setup
 * @returns Promise resolving to validation result
 * @throws {InstallationError} When installation path is invalid
 */
async function validateInstallation(
  installPath: string,
  options: OfflineSetupOptions
): Promise<ValidationResult> {
  // Implementation...
}
```

## 🎯 Gaming-Specific Guidelines

### Performance Considerations
- **Minimize setup time** - keep installation process under 5 minutes
- **Reduce file size** - optimize downloads and avoid bloated dependencies
- **Support low-end hardware** - ensure compatibility with minimum specs
- **Handle interruptions gracefully** - support resume for long operations

### User Experience
- **Clear progress indicators** throughout setup process
- **Helpful error messages** with actionable solutions
- **Rollback capability** for failed installations
- **Backup existing saves** before making changes

### Platform Support
- **Windows 10/11** - Primary target platform
- **macOS 10.15+** - Including Apple Silicon support
- **Linux Ubuntu/Debian** - Focus on popular distributions
- **Steam Deck** - Optimize for handheld gaming

## 🎮 Gaming Community Guidelines

### Community Standards
- **Be respectful** to all community members
- **Help newcomers** with setup and troubleshooting
- **Share knowledge** about Illuvium game mechanics
- **Report bugs constructively** with helpful details

### Content Guidelines
- **Game content spoilers** should be clearly marked
- **Respect intellectual property** of Illuvium Labs
- **No piracy discussion** - focus on legitimate offline access
- **Keep discussions gaming-focused** and project-relevant

## 🔐 Security Considerations

### Code Security
- **No hardcoded credentials** or API keys
- **Validate all user inputs** to prevent injection attacks
- **Use secure file operations** when modifying game files
- **Implement proper error handling** to avoid information leaks

### User Privacy
- **No telemetry collection** without explicit consent
- **Local-only operations** - avoid unnecessary network calls
- **Secure credential storage** for optional online features
- **Clear privacy policy** for any data collection

## 📊 Release Process

### Version Management
- **Semantic versioning** (MAJOR.MINOR.PATCH)
- **Changelog maintenance** for all releases
- **Pre-release testing** on all supported platforms
- **GitHub releases** with downloadable binaries

### Release Checklist
- [ ] All tests passing on CI/CD
- [ ] Documentation updated
- [ ] Changelog updated
- [ ] Version numbers incremented
- [ ] Platform binaries built and tested
- [ ] Release notes prepared
- [ ] Community announcement ready

## 🆘 Getting Help

### Support Channels
- **GitHub Issues** - Bug reports and feature requests
- **Discord Community** - Real-time help and discussions
- **Reddit r/illuvium** - Community support and tips
- **Documentation** - Comprehensive setup guides

### Mentorship Program
New contributors can request mentorship for:
- **First-time contributions** to open source
- **Gaming industry development** practices
- **Cross-platform development** techniques
- **Community management** and communication

## 🏆 Recognition

### Contributor Acknowledgments
- **README credits** for significant contributions
- **Release notes mentions** for featured improvements
- **Community spotlight** in Discord and social media
- **Maintainer status** for sustained contributions

### Hall of Fame
Special recognition for contributors who have made exceptional impact:
- **Core maintainers** who keep the project running
- **Community leaders** who help others and build engagement
- **Innovation contributors** who add groundbreaking features
- **Documentation heroes** who make the project accessible

---

## 📞 Contact

- **Project Maintainers**: @iluvium-io team
- **Discord**: [Illuvium Community](https://discord.gg/illuvium)
- **Email**: contribute@iluvium-io.github.io
- **Twitter**: [@illuviumio](https://twitter.com/illuviumio)

Thank you for helping make Illuvium more accessible to the gaming community! 🎮✨ 