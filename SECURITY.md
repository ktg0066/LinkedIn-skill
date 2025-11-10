# Security Policy

## 🔒 Data Privacy & Security

The LinkedIn Thought Leadership Skill is designed with your privacy in mind. This document outlines our security practices and how to report vulnerabilities.

---

## 🛡️ What Data Is Stored

### Local Only (Never Shared)
All your personal data stays **on your device** in the skill folder:
- Your personalization settings
- Your voice samples
- Your successful post examples
- Your frameworks and case studies
- Your audience insights and analytics
- Any populated asset folders

**We do not:**
- ❌ Collect any user data
- ❌ Send data to external servers
- ❌ Track your usage
- ❌ Store your LinkedIn credentials
- ❌ Access your LinkedIn account

### What Gets Shared with Claude
When you use the skill, only the content you explicitly share in your prompts is sent to Claude (Anthropic):
- Your requests ("Write a post about...")
- Content from the skill files you're using
- Your responses to Claude

This follows standard Claude usage patterns. See [Anthropic's Privacy Policy](https://www.anthropic.com/privacy) for details.

---

## 🔐 Best Practices for Users

### Protecting Your Personal Data

1. **Never commit personal data to public repositories**
   - The `.gitignore` file is pre-configured to exclude your personal assets
   - Review before committing if you fork this repo

2. **Be cautious when sharing examples**
   - Anonymize any company names, client information, or personal details
   - Remove specific metrics that could identify your organization
   - Sanitize case studies before sharing publicly

3. **Secure your tokens and credentials**
   - Never include API keys in asset files
   - Don't store LinkedIn credentials in the skill folder
   - Keep GitHub tokens secure if contributing

4. **Regular backups**
   - Back up your populated asset folders regularly
   - Store backups securely (encrypted drives recommended)
   - Keep backups separate from public repositories

### When Contributing

If you contribute templates or examples:
- ✅ Anonymize all personal and company data
- ✅ Remove specific metrics, names, and identifiers
- ✅ Replace with generic placeholders like [Company], [X metrics], etc.
- ✅ Review your contribution for any personally identifiable information (PII)

---

## 🐛 Reporting Security Vulnerabilities

We take security seriously. If you discover a security vulnerability, please follow responsible disclosure:

### What to Report

Please report issues related to:
- Unintended data exposure or leakage
- Vulnerabilities in templates that could expose user data
- Security flaws in documentation that could mislead users
- Dependencies with known security issues

### How to Report

**For security vulnerabilities, do NOT use public GitHub Issues.**

Instead:
1. **Email:** kjell.tore.guttormsen@gmail.com
2. **Subject:** "SECURITY: LinkedIn Skill - [Brief Description]"
3. **Include:**
   - Description of the vulnerability
   - Steps to reproduce
   - Potential impact
   - Suggested fix (if any)

### Response Timeline

- **Initial response:** Within 48 hours
- **Status update:** Within 7 days
- **Fix timeline:** Depends on severity
  - **Critical:** Within 7 days
  - **High:** Within 14 days
  - **Medium:** Within 30 days
  - **Low:** Next scheduled release

### Recognition

Security researchers who responsibly disclose vulnerabilities will be:
- Acknowledged in CHANGELOG.md (with permission)
- Added to security contributors list in README.md
- Credited in the fix commit message

---

## 🔍 Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | ✅ Full support    |
| 0.9.x   | ⚠️ Security fixes only |
| < 0.9   | ❌ No longer supported |

We recommend always using the latest version for security and features.

---

## 🚨 Known Limitations

### Not Security Issues
The following are **known limitations** and **not security vulnerabilities**:

1. **Data is stored locally in plain text**
   - This is by design for easy editing and transparency
   - Users are responsible for securing their device
   - Recommend encrypted drives for sensitive data

2. **No built-in encryption**
   - The skill is markdown-based for accessibility
   - Users can encrypt their asset folders externally if needed
   - System-level encryption (FileVault, BitLocker) is recommended

3. **Claude processes your data**
   - This is inherent to using any Claude skill
   - Governed by Anthropic's privacy policy
   - Users control what prompts they send

---

## 📚 Security Resources

### For Users
- [Anthropic Privacy Policy](https://www.anthropic.com/privacy)
- [Claude Desktop Security](https://support.anthropic.com/en/articles/security)
- [Data Privacy Best Practices](https://www.anthropic.com/security)

### For Contributors
- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [GitHub Security Best Practices](https://docs.github.com/en/code-security)
- [Markdown Security Considerations](https://github.github.com/gfm/#security-considerations)

---

## 🔄 Security Updates

Security updates will be:
1. **Released immediately** for critical vulnerabilities
2. **Announced** in CHANGELOG.md with **[SECURITY]** tag
3. **Documented** in GitHub Security Advisories
4. **Communicated** via GitHub discussions for major issues

---

## 📝 Security Checklist for Contributors

Before submitting a pull request:

- [ ] I have not included any API keys, tokens, or credentials
- [ ] I have anonymized all personal and company data in examples
- [ ] I have reviewed my changes for potential data exposure
- [ ] I have not added dependencies with known vulnerabilities
- [ ] I have followed secure coding practices
- [ ] I have documented any security considerations for users

---

## ⚖️ Disclosure Policy

**We believe in responsible disclosure:**

1. Security researchers report privately
2. We acknowledge receipt and investigate
3. We develop and test fixes
4. We release security update
5. We publicly disclose details after fix is available
6. We credit researchers (with permission)

**Timeline:** 90 days from report to public disclosure (or sooner if critical)

---

## 🤝 Questions?

For security questions or clarifications:
- **Private security matters:** kjell.tore.guttormsen@gmail.com
- **General security questions:** [GitHub Discussions](https://github.com/ktg0066/LinkedIn-skill/discussions)
- **Non-security bugs:** [GitHub Issues](https://github.com/ktg0066/LinkedIn-skill/issues)

---

## 📜 Changes to This Policy

We may update this security policy. Changes will be:
- Documented in CHANGELOG.md
- Announced in GitHub discussions for major changes
- Effective immediately upon commit to main branch

**Last updated:** 2025-11-10

---

Thank you for helping keep the LinkedIn Thought Leadership Skill secure! 🙏

Your responsible disclosure helps protect all users.
