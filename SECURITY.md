# Security Policy

## Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| 1.x.x   | ✅                 |
| < 1.0   | ❌                 |

## Reporting a Vulnerability

We take security seriously. If you discover a security vulnerability, please report it responsibly.

### How to Report

1. **DO NOT** create a public GitHub issue for security vulnerabilities
2. Send a detailed description to: **your.email@example.com**
3. Include:
   - Description of the vulnerability
   - Steps to reproduce (PoC if possible)
   - Potential impact assessment
   - Suggested fix (if any)

### Response Timeline

- **Acknowledgment:** Within 48 hours
- **Assessment:** Within 1 week
- **Fix/Resolution:** Within 2 weeks (for critical/high severity)
- **Disclosure:** Coordinated with reporter after fix is released

### Security Best Practices for This Project

This project follows these security standards:
- Regular dependency updates via Dependabot
- Automated secret scanning (gitleaks)
- Static Application Security Testing (Semgrep)
- No secrets in environment variables or code
- Least-privilege access principle

## Security Headers (for web services)

```yaml
X-Content-Type-Options: nosniff
X-Frame-Options: DENY
X-XSS-Protection: 1; mode=block
Strict-Transport-Security: max-age=31536000; includeSubDomains
Content-Security-Policy: default-src 'self'
```

## Additional Resources

- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [GitHub Security Advisories](https://docs.github.com/en/code-security/security-advisories)
