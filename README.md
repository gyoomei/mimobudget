<div align="center">

# 💰 MiMoBudget
### AI-Powered Personal Expense Tracker & Financial Advisor

<p>
<img src="https://img.shields.io/badge/Built_with-Xiaomi_MiMo_V2.5-FF6900?style=for-the-badge&logo=xiaomi&logoColor=white">
<img src="https://img.shields.io/badge/Type-Single_HTML-6366F1?style=for-the-badge&logo=html5&logoColor=white">
<img src="https://img.shields.io/badge/Dependencies-Zero-10B981?style=for-the-badge&logo=node.js&logoColor=white">
</p>

<p>
<img src="https://img.shields.io/github/stars/gyoomei/mimobudget?style=flat-square&color=FFD700">
<img src="https://img.shields.io/github/last-commit/gyoomei/mimobudget?style=flat-square&color=6366F1">
<img src="https://img.shields.io/github/license/gyoomei/mimobudget?style=flat-square&color=10B981">
<img src="https://img.shields.io/badge/Powered_by-Pollinations.ai-blue?style=flat-square">
</p>

**[Live Demo](https://gyoomei.github.io/mimobudget/)** · **[Report Bug](https://github.com/gyoomei/mimobudget/issues)** · **[Request Feature](https://github.com/gyoomei/mimobudget/issues)**

</div>

---

## 🎯 The Problem

Personal finance apps are either too complex (Mint, YNAB) or too simple (basic calculators). Most require accounts, subscriptions, and bank linking. Indonesian users especially struggle with apps that don't understand local currency patterns like "25k", "1.5jt", or "Rp 50.000".

**What if your expense tracker understood you — in your own language?**

## ✨ The Solution

MiMoBudget is a zero-dependency, single-file AI expense tracker that speaks your language. Type "kopi 15k" and it knows: that's a food expense of Rp 15,000. Ask "tips hemat" and Xiaomi MiMo analyzes your spending pattern to give personalized advice.

**That's the entire UX.**

---

## 🚀 Features

### 💬 Natural Language Input
Type expenses the way you think — no forms, no dropdowns, no friction.
```
"kopi 15k"          → ☕ Food & Drink: Rp 15k
"grab 35rb"         → 🚗 Transport: Rp 35k
"gaji 5jt"          → 💰 Income: Rp 5jt
"token listrik 200k" → 📄 Bills: Rp 200k
```
Smart parser auto-detects category from keywords and converts Indonesian number formats (k, rb, jt, juta).

### 📊 Visual Analytics
- **Doughnut chart** — spending breakdown by category
- **Daily bar chart** — 7-day spending trend
- **Monthly line chart** — income vs expense over 6 months

### 💰 Budget Limits
Set monthly limits per category. Visual progress bars show at-a-glance:
- 🟢 Green: under 70%
- 🟡 Yellow: 70-90%
- 🔴 Red: over 90%

### 🎯 Savings Goals
Track progress toward financial goals with visual milestone bars. Add savings incrementally and watch progress grow.

### 🤖 MiMo AI Advisor
Ask Xiaomi MiMo V2.5 anything about your finances:
- "Analisis spending saya bulan ini"
- "Tips hemat untuk kategori pengeluaran terbesar"
- "Buatkan rencana budget bulanan"
- "Kategori apa yang perlu dikurangi?"

MiMo has full context of your transactions, budgets, and goals — so advice is personalized, not generic.

### 🌓 Dark & Light Theme
Premium dark mode with animated mesh gradient + floating particles. Clean light mode for daytime use. Toggle persists via localStorage.

### 📥 Data Export
Export all transactions as CSV with one click. Full data ownership — everything stays in localStorage, nothing sent to any server.

---

## 📸 Screenshots

<div align="center">

| Dark Theme — Dashboard | Charts & Analytics |
|:---:|:---:|
| ![Dashboard](https://gyoomei.github.io/mimobudget/) | ![Charts](https://gyoomei.github.io/mimobudget/) |

| Budget & Goals | AI Advisor Chat |
|:---:|:---:|
| ![Budget](https://gyoomei.github.io/mimobudget/) | ![Chat](https://gyoomei.github.io/mimobudget/) |

</div>

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────┐
│              MiMoBudget v1.0                │
│         Single HTML · Zero Backend          │
├─────────────────────────────────────────────┤
│                                             │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  │
│  │  NLP      │  │ Budget   │  │  Goals   │  │
│  │  Parser   │  │ Engine   │  │ Tracker  │  │
│  │(Indonesian│  │(Limits + │  │(Savings +│  │
│  │ + English)│  │ Progress)│  │ Milestone│  │
│  └────┬─────┘  └────┬─────┘  └────┬─────┘  │
│       │              │              │        │
│  ┌────▼──────────────▼──────────────▼────┐  │
│  │          localStorage                 │  │
│  │   (Zero server · Full data ownership) │  │
│  └────────────────┬──────────────────────┘  │
│                   │                         │
│  ┌────────────────▼──────────────────────┐  │
│  │         Chart.js Visualizations       │  │
│  │  Doughnut · Bar · Line (3 chart types) │  │
│  └────────────────┬──────────────────────┘  │
│                   │                         │
│  ┌────────────────▼──────────────────────┐  │
│  │     Pollinations.ai (Free API)        │  │
│  │   Xiaomi MiMo V2.5 · Chat Advisor     │  │
│  └───────────────────────────────────────┘  │
│                                             │
└─────────────────────────────────────────────┘
```

---

## ⚡ Performance

| Metric | Value |
|--------|-------|
| File size | 36 KB (single HTML) |
| Dependencies | 0 (CDN: Chart.js + Google Fonts) |
| Load time | < 1s on 3G |
| AI response | 3-8s (Pollinations.ai) |
| Data storage | localStorage (unlimited for most browsers) |
| Offline support | Full (except AI chat) |

---

## 🔒 Security & Privacy

- **Zero backend** — no data leaves your browser
- **No accounts** — no email, no password, no tracking
- **No analytics** — no Google Analytics, no Plausible, no Clarity
- **localStorage only** — data stays on your device
- **API calls** — only to Pollinations.ai for AI chat (no user data sent, only financial summary context)
- **Open source** — auditable single-file HTML

---

## 🛠️ Local Development

```bash
# Clone
git clone https://github.com/gyoomei/mimobudget.git
cd mimobudget

# Open directly
open index.html

# Or serve locally
python3 -m http.server 8080
# → http://localhost:8080
```

No build step. No npm install. No config. Just open and go.

---

## 🤝 Contributing

Contributions welcome! Ideas:
- [ ] Multi-currency support (USD, EUR, MYR, SGD)
- [ ] Recurring transaction templates
- [ ] Bill reminders with notifications
- [ ] Import from bank CSV exports
- [ ] Spending forecast with ML
- [ ] Indonesian bank e-wallet integration (GoPay, OVO, DANA)

---

## 📄 License

MIT — use it, fork it, make it yours.

---

<div align="center">

**Built with ❤️ for the [Xiaomi MiMo 100T Creator Program](https://mimo-100t.com)**

<img src="https://img.shields.io/badge/Made_by-gyoomei-6366F1?style=for-the-badge&logo=github&logoColor=white">

</div>
