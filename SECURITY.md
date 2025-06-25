# Security Policy 🔐

## 🛡️ Supported Versions

We actively maintain and provide security updates for the following versions:

| Version | Supported          | End of Life |
| ------- | ------------------ | ----------- |
| 1.2.x   | ✅ Yes             | TBD         |
| 1.1.x   | ✅ Yes (Critical)  | 2024-12-31  |
| 1.0.x   | ❌ No              | 2024-06-30  |
| < 1.0   | ❌ No              | 2024-01-31  |

**Note**: Only the latest two minor versions receive full security support. Critical security issues may be backported to older versions at maintainer discretion.

## 🚨 Reporting a Vulnerability

### 🔒 Responsible Disclosure

If you discover a security vulnerability in the Illuvium Offline Setup Assistant, please report it responsibly:

**DO NOT** create a public GitHub issue for security vulnerabilities.

### 📧 Security Contact

Send security reports to: **security@iluvium-io.github.io**

Include the following information:
- **Vulnerability description** and potential impact
- **Steps to reproduce** the security issue
- **Affected versions** and platforms
- **Proof of concept** (if applicable)
- **Suggested fix** (if you have one)

### ⏰ Response Timeline

- **Acknowledgment**: Within 48 hours
- **Initial assessment**: Within 1 week
- **Status update**: Weekly during investigation
- **Fix deployment**: 2-4 weeks (depending on severity)
- **Public disclosure**: After fix deployment

### 🏆 Security Researcher Recognition

We maintain a Hall of Fame for security researchers who help improve our project security:
- Public acknowledgment (with permission)
- Credit in release notes
- Special contributor status

## 🎯 Security Scope

### ✅ In Scope
- **Setup assistant vulnerabilities** that could compromise user systems
- **File system security** issues during installation process
- **Code injection** vulnerabilities in setup scripts
- **Privilege escalation** during administrative operations
- **Data privacy** issues with user information
- **Supply chain** vulnerabilities in dependencies

### ❌ Out of Scope
- **Illuvium game vulnerabilities** (report to Illuvium Labs)
- **Epic Games launcher** security issues
- **Third-party tools** bundled with the setup
- **Social engineering** attacks
- **Physical access** to user devices
- **DoS attacks** against our infrastructure

## 🔐 Security Measures

### Code Security
- **Static analysis** with CodeQL and SonarCloud
- **Dependency scanning** for known vulnerabilities
- **Signed releases** with verified checksums
- **Minimal permissions** - principle of least privilege
- **Input validation** for all user-provided data

### Build Security
- **Reproducible builds** with locked dependency versions
- **Secure CI/CD** pipeline with isolated environments
- **Multi-platform** security testing
- **Code signing** for Windows and macOS binaries
- **Supply chain verification** for all dependencies

### Runtime Security
- **Sandboxed operations** where possible
- **Secure file handling** with proper permission checks
- **Network isolation** for offline-focused operations
- **Error handling** that doesn't leak sensitive information
- **Automatic cleanup** of temporary files and credentials

## 🎮 Gaming-Specific Security

### Game File Integrity
- **Checksum verification** of game files
- **Backup creation** before modification
- **Rollback capability** for failed installations
- **Safe file patching** without corrupting game data

### User Privacy
- **No telemetry** collection by default
- **Local operation** - minimal network communication
- **Secure credential storage** (if optional features require it)
- **Clear data handling** policies

### Platform Security
- **Windows**: UAC integration, signed drivers when needed
- **macOS**: Gatekeeper compatibility, notarized binaries
- **Linux**: Package manager integration, proper permissions

## 🛠️ Security Best Practices for Contributors

### Development Guidelines
```bash
# Always validate inputs
function validatePath(userPath: string): boolean {
  // Prevent directory traversal
  const normalized = path.normalize(userPath);
  return !normalized.includes('..');
}

# Use secure file operations
async function secureFileWrite(filePath: string, content: string) {
  // Verify write permissions first
  await fs.access(path.dirname(filePath), fs.constants.W_OK);
  // Use atomic write operations
  await fs.writeFile(filePath + '.tmp', content);
  await fs.rename(filePath + '.tmp', filePath);
}
```

### Dependency Management
- **Regular updates** of security-critical dependencies
- **Vulnerability scanning** before adding new dependencies
- **Minimal dependency tree** to reduce attack surface
- **License compatibility** verification

### Testing Security
```typescript
describe('Security Tests', () => {
  it('should prevent directory traversal', () => {
    const maliciousPath = '../../../etc/passwd';
    expect(() => validateInstallPath(maliciousPath)).toThrow();
  });
  
  it('should handle large files safely', () => {
    const oversizedInput = 'x'.repeat(10_000_000);
    expect(() => processUserInput(oversizedInput)).not.toThrow();
  });
});
```

## 🚨 Known Security Considerations

### Administrative Privileges
The setup assistant requires administrative privileges for:
- **Installing system-level dependencies**
- **Modifying game installation directories**
- **Creating symbolic links** (on Unix systems)
- **Registering file associations**

**Mitigation**: Operations are scoped to minimum required privileges and validated before execution.

### Third-Party Dependencies
We use several third-party libraries:
- **Package managers**: npm, yarn
- **Compression**: 7-zip, unrar
- **System tools**: Platform-specific utilities

**Mitigation**: All dependencies are scanned for vulnerabilities and updated regularly.

### Network Operations
Minimal network access is used for:
- **Update checking** (optional)
- **Dependency downloading** during setup
- **Error reporting** (with user consent)

**Mitigation**: All network operations can be disabled for fully offline usage.

## 📋 Security Checklist for Releases

Before each release, we verify:

- [ ] **Dependencies updated** to latest secure versions
- [ ] **Security scan** completed with no critical issues
- [ ] **Code signing** applied to all platform binaries
- [ ] **Checksums generated** and verified for downloads
- [ ] **Privacy policy** updated if data handling changes
- [ ] **Security documentation** reviewed and updated
- [ ] **Penetration testing** completed for major releases

## 🔍 Vulnerability Disclosure Timeline

### Recent Security Updates

**v1.2.1** (2024-01-15)
- Fixed path traversal vulnerability in file extraction
- Updated dependencies with security patches
- Enhanced input validation for user-provided paths

**v1.1.3** (2023-12-01)
- Resolved privilege escalation issue on Windows
- Improved error handling to prevent information disclosure
- Added additional permission checks for file operations

## 📞 Emergency Contact

For critical security issues requiring immediate attention:

- **Email**: security-urgent@iluvium-io.github.io
- **Response time**: Within 24 hours
- **Escalation**: Project maintainers will be notified immediately

## 🔗 Additional Resources

- [OWASP Secure Coding Practices](https://owasp.org/www-project-secure-coding-practices-quick-reference-guide/)
- [GitHub Security Advisories](https://github.com/advisories)
- [National Vulnerability Database](https://nvd.nist.gov/)
- [Gaming Security Best Practices](https://www.nist.gov/cybersecurity)

---

**Remember**: Security is everyone's responsibility. If you see something, say something! 🛡️ 