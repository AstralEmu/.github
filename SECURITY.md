# Security Policy

## Supported Versions

Only the latest version of each AstralEmu image and package repository is supported with security updates. Images are rebuilt every 24 hours, which means security patches from upstream distributions are integrated automatically within one rebuild cycle.

| Component | Supported |
|---|---|
| Latest image builds | Yes |
| Package repositories (latest) | Yes |
| Older image builds | No — rebuild or update to latest |

## Reporting a Vulnerability

If you discover a security vulnerability in AstralEmu, **do not open a public issue**.

Instead, please report it privately:

1. Go to the affected repository on GitHub
2. Click on the **Security** tab
3. Click **Report a vulnerability** (GitHub Security Advisories)
4. Provide as much detail as possible

### What to Include

- Description of the vulnerability
- Steps to reproduce
- Affected component (image builder, package build, performance manager, service management, etc.)
- Affected device(s) and base distribution if relevant
- Potential impact

### What to Expect

- **Acknowledgment** within 72 hours
- **Assessment** within 1 week
- **Fix or mitigation** in the next rebuild cycle when possible
- Credit in the release notes (unless you prefer to remain anonymous)

## Scope

The following are in scope for security reports:

- **Image builder**: Workflow injection, supply chain issues in build pipelines
- **Package builds**: Compromised build dependencies, unsigned packages, build tampering
- **Performance manager**: Privilege escalation via governor/overclock controls
- **Service management**: Unintended service exposure, isolation bypass between services (ES-DE, XFCE, Plasma Mobile, Kodi, Waydroid)
- **Update mechanism**: Man-in-the-middle on updates, unsigned image delivery
- **Cross-distro translation**: Dependency confusion, malicious package substitution

The following are **out of scope**:

- Vulnerabilities in upstream emulators (report to the emulator project directly)
- Vulnerabilities in upstream distributions (report to Ubuntu, Debian, Fedora, or Arch directly)
- Vulnerabilities requiring physical access to a device that is already unlocked
- Social engineering attacks

## Security Practices

AstralEmu follows these security practices:

- All packages are built from source in GitHub Actions — no pre-built binaries from untrusted sources
- Build pipelines include verification to prevent re-download or re-upload of tampered artifacts
- Overclock safety limits are enforced based on power supply status
- Only one service runs at a time, reducing attack surface
