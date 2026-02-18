# Do Not Use XMRWallet.com

![xmrwallet.com scam warning](docs/img/banner.svg)

This repository documents confirmed security issues with **www.xmrwallet.com**.

⚠️ **[View the full evidence page →](https://phishdestroy.github.io/DO-NOT-USE-xmrwallet-com/)**

## What's documented here

- Private view key exfiltration (40+ requests per session)
- Google Analytics + Tag Manager on a "private" wallet
- Self-phishing infrastructure / typosquat domains
- DDoS-Guard hosting to evade takedowns
- Victim reports (590 XMR, 17 XMR, multiple accounts)
- Deleted GitHub issues and fake Trustpilot reviews

## Quick proof

```python
import base64
# Decode part of any session_key from a live session:
print(base64.b64decode("ZWZiYTEzZWNiOGIzNjA2NjBhM2RjYWFmYWY3Y2Y5OTE0OTcxM2QwNjRiOWQ2NDk5N2IyNDU0ZDU4ZWU2NzgwMA==").decode())
# → efba13ecb8b360660a3dcaafaf7cf99149713d064b9d64997b2454d58ee67800
#   ↑ private view key transmitted in session_key on every API request
```

## If you lost funds

See [LOST_FUNDS.md](LOST_FUNDS.md) — checklist, explorer links, all report URLs.

## Technical evidence

- [Issue #36](https://github.com/XMRWallet/Website/issues/36) — view key exfiltration proof
- [Issue #35](https://github.com/XMRWallet/Website/issues/35) — additional findings
- [proof/TECHNICAL_EVIDENCE.md](proof/TECHNICAL_EVIDENCE.md)
- [proof/GOOGLE_ANALYTICS_AND_VICTIMS.md](proof/GOOGLE_ANALYTICS_AND_VICTIMS.md)

## Use instead

- **Official Monero GUI** → https://getmonero.org/downloads
- **Feather Wallet** → https://featherwallet.org

---

*Research by [PhishDestroy](https://github.com/phishdestroy) · [destroylist](https://github.com/phishdestroy/destroylist) — 70,000+ blocked domains*
