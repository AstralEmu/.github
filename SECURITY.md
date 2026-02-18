<p align="center">
  <img src="https://raw.githubusercontent.com/AstralEmu/.github/main/profile/banner-astralemu.svg" alt="AstralEmu" width="100%"/>
</p>

<h1 align="center">Security Policy</h1>

<p align="center">
  <i>How to report vulnerabilities and what to expect.</i>
</p>

---

## Supported Versions

Only the latest version of each AstralEmu image and package repository is supported with security updates. Images are rebuilt every 24 hours, which means security patches from upstream distributions are integrated automatically within one rebuild cycle.

| Component | Supported |
|---|---|
| Latest image builds | Yes |
| Package repositories (latest) | Yes |
| Older image builds | No — rebuild or update to latest |

## Reporting a Vulnerability

> **Do not open a public issue for security vulnerabilities.**

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

| Step | Timeline |
|---|---|
| Acknowledgment | Within 72 hours |
| Assessment | Within 1 week |
| Fix or mitigation | Next rebuild cycle when possible |
| Credit in release notes | Unless you prefer to remain anonymous |

---

## Scope

### In Scope

| Component | Examples |
|---|---|
| **Image builder** | Workflow injection, supply chain issues in build pipelines |
| **Package builds** | Compromised build dependencies, unsigned packages, build tampering |
| **Performance manager** | Privilege escalation via governor/overclock controls |
| **Service management** | Unintended service exposure, isolation bypass between ES-DE, XFCE, Plasma Mobile, Kodi, Waydroid |
| **Update mechanism** | Man-in-the-middle on updates, unsigned image delivery |
| **Cross-distro translation** | Dependency confusion, malicious package substitution |

### Out of Scope

- Vulnerabilities in upstream emulators — report to the emulator project directly
- Vulnerabilities in upstream distributions — report to Ubuntu, Debian, Fedora, or Arch directly
- Vulnerabilities requiring physical access to a device that is already unlocked
- Social engineering attacks

---

## Security Practices

AstralEmu follows these security practices:

- All packages are built from source in GitHub Actions — no pre-built binaries from untrusted sources
- Build pipelines include verification to prevent re-download or re-upload of tampered artifacts
- Overclock safety limits are enforced based on power supply status
- Only one service runs at a time, reducing attack surface

---

<p align="center">
  <a href="https://astralemu.github.io">Documentation</a> &middot;
  <a href="https://github.com/orgs/AstralEmu/discussions">Community</a> &middot;
  <a href="https://github.com/AstralEmu/astralemu">Main Repository</a>
</p>
