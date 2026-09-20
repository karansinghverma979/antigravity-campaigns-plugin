# Security Policy

## Supported Versions
Only the latest release receives active security updates and patches.

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | :white_check_mark: |
| < 1.0.0 | :x:                |

## Security Directives & Data Isolation
- **Local SQLite Isolation**: The database runtime state (`campaigns.sqlite`) resides strictly outside the repository tree (defaulting to `%APPDATA%\Campaigns\Database\` on Windows and `~/.local/share/campaigns/` on Unix).
- **Zero Absolute Paths**: Code and documentation must never contain machine-specific paths or user credentials.
- **MCP Whitelist Boundary**: Database operations execute strictly through parameter-validated MCP handlers without raw string concatenation or arbitrary shell execution.

## Reporting a Vulnerability
**Please do not report security vulnerabilities through public GitHub issues.**

To report a vulnerability:
1. Use GitHub's private vulnerability advisory reporting:
   `https://github.com/karansinghverma979/antigravity-campaigns-plugin/security/advisories/new`
2. Maintainers will respond within 48 hours and coordinate a remediated release.
