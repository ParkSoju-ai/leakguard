# 🛡️ LeakGuard

**Scan your own GitHub repo for exposed secrets before someone else finds them.**

LeakGuard is a free, open-source browser tool that scans public GitHub repositories for accidentally committed API keys, passwords, tokens, and other secrets — then tells you exactly where they are and how to fix them.

> ⚠️ **For scanning your own repositories only. Use responsibly.**

---

## 🚀 Live Demo

👉 **[Try it now → ParkSoju-ai.github.io/leakguard](https://ParkSoju-ai.github.io/leakguard)**

---

## 📸 Screenshot

![LeakGuard Screenshot](screenshot.png)

---

## 🔍 What It Detects

| Secret Type | Severity |
|---|---|
| OpenAI / Anthropic API Keys | 🔴 Critical |
| AWS Access & Secret Keys | 🔴 Critical |
| Google API Keys | 🔴 Critical |
| GitHub Tokens | 🔴 Critical |
| Stripe Live Keys | 🔴 Critical |
| Telegram Bot Tokens | 🔴 Critical |
| Slack Tokens | 🔴 Critical |
| Slack Webhooks | 🔴 Critical |
| Hardcoded Passwords | 🔴 Critical |
| Database Connection Strings | 🔴 Critical |
| Private Key Blocks (RSA/EC) | 🔴 Critical |
| JWT Secrets | 🔴 Critical |
| Cloudflare API Tokens | 🔴 Critical |
| Shopee / Lazada Affiliate Tokens | 🔴 Critical |
| Stripe Test Keys | 🟡 Warning |
| Firebase Config Keys | 🟡 Warning |
| Generic Secrets & API Keys | 🟡 Warning |
| `.env` file committed | 🟡 Warning |

---

## ✨ Features

- ✅ **100% browser-based** — no server, no backend, no data stored
- ✅ **No login required** — works with any public GitHub repo
- ✅ **20+ secret patterns** detected
- ✅ **Git history scan** — finds secrets that were committed and later deleted, since they remain permanently in git history even after removal from the current code
- ✅ **Optional GitHub token** — raises the API limit from 60 → 5,000 requests/hour and enables scanning your own private repos; the token stays in memory for the session only and is never stored, logged, or sent anywhere but `api.github.com`
- ✅ **Shows exact file + line number** of each issue, plus commit SHA/author/date for history findings
- ✅ **Tells you how to fix** every finding
- ✅ **Scans up to 80 files** per repo via GitHub's public API
- ✅ **Prioritizes sensitive files** like `.env`, `config.js`, `secrets.js`
- ⚠️ **GitHub API limit** — unauthenticated scans are limited to 60 requests/hour. Git history scanning uses roughly 1 request per commit checked, so it can exhaust the free limit quickly — add a personal access token to scan comfortably.

---

## 🛠️ How to Use

1. Go to **[ParkSoju-ai.github.io/leakguard](https://ParkSoju-ai.github.io/leakguard)**
2. Paste your GitHub repo URL (e.g. `https://github.com/yourname/yourrepo`)
3. *(Optional)* Check **"Include Git History Scan"** to also check past commits for secrets that were deleted from the current code
4. *(Optional)* Paste a [personal access token](https://github.com/settings/tokens) to raise the rate limit and enable private-repo scanning — it's free, stays in your browser's memory only, and is used solely for requests to `api.github.com`
5. Click **[ EXECUTE SCAN ]**
6. Review findings and follow the fix instructions

That's it — no install, no sign up, no tracking.

---

## 🖥️ Run Locally

Just download and open:

```bash
git clone https://github.com/ParkSoju-ai/leakguard.git
cd leakguard
# Open index.html in your browser
```

No dependencies. No build step. Pure HTML/CSS/JS.

---

## 🔒 Privacy

- LeakGuard runs **entirely in your browser**
- It only reads **publicly accessible files and commits** via GitHub's API, or private repo data you explicitly authorize with your own token
- If provided, your GitHub token is held **only in browser memory for that session** — never stored, logged, written to disk, or sent to anything but `api.github.com`
- It does **not store, log, or transmit** any scan data
- No cookies, no analytics, no tracking

---

## ⚠️ Responsible Use

LeakGuard is built for developers to audit **their own repositories** before publishing. Using this tool to scan repositories you do not own may violate GitHub's Terms of Service and local laws.

**Scan your own repos. Be responsible.**

---

## 🤝 Contributing

Found a new secret pattern to detect? PRs are welcome!

1. Fork the repo
2. Add your pattern to the `PATTERNS` array in `index.html`
3. Submit a pull request

---

## 💛 Support This Project

If LeakGuard saved your API key from being stolen, consider supporting:

[![GitHub Sponsors](https://img.shields.io/badge/Sponsor-%E2%9D%A4-pink?logo=github)](https://github.com/sponsors/ParkSoju-ai)

---

## 📄 License

MIT License — free to use, modify, and distribute.

---

*Built with ❤️ by [@ParkSoju-ai](https://github.com/ParkSoju-ai)*
