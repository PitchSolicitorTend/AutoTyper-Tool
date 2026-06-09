# Security Policy

## Supported Versions

The following versions of AutoTyper Tool currently receive security updates:

| Version | Supported          |
| ------- | ------------------ |
| 2.5.x   | ✅ Yes              |
| 2.0.x   | ✅ Yes              |
| 1.5.x   | ⚠️ Critical fixes only |
| < 1.5   | ❌ No               |

## Reporting a Vulnerability

If you discover a security vulnerability in AutoTyper Tool, **please do not open a public issue**.

Instead:

1. Open a [private security advisory](https://github.com/PitchSolicitorTend/fwycbzlv/security/advisories/new) on GitHub, **or**
2. Open a regular issue with minimal details and a note asking a maintainer to follow up privately.

Please include:

- A description of the vulnerability and its potential impact
- Steps to reproduce (proof of concept, if available)
- The version of AutoTyper Tool affected
- Your Windows version

### What to Expect

- We aim to acknowledge reports within **5 business days**.
- We will investigate and, if confirmed, work on a fix and coordinate a release timeline with you.
- Once a fix is released, we will credit you in [CHANGELOG.md](CHANGELOG.md) (unless you prefer to remain anonymous).

## Scope Notes

AutoTyper Tool:

- Does **not** make any network requests.
- Does **not** collect, store, or transmit any user data or typed text.
- Runs entirely locally on the user's machine.

Reports related to **false-positive antivirus/SmartScreen detections** are not security vulnerabilities — see the FAQ in [README.md](README.md#frequently-asked-questions) and [docs/installation.md](docs/installation.md) for an explanation of why keyboard-automation tools are sometimes flagged.
