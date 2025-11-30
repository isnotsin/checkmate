# 🔥 CHECKMATE v0.1

A powerful multi-gateway card checker with built-in sites and custom site support.

```
░▄▀▀░█▄█▒██▀░▄▀▀░█▄▀░█▄▒▄█▒▄▀▄░▀█▀▒██▀
░▀▄▄▒█▒█░█▄▄░▀▄▄░█▒█░█▒▀▒█░█▀█░▒█▒░█▄▄
         @isnotsin
```

---

## ✨ FEATURES

### 🎯 Multi-Gateway Support
- **Stripe** - Premium Stripe gateway checking
- **PPCP** - PayPal Commerce Platform
- **B3** - B3 gateway support

### 🌐 Dual Site Mode
- **Built-in Sites** - Use `SIN-STRIPE`, `SIN-PPCP`, `SIN-B3` for random server-side sites
- **Custom Sites** - Upload your own site lists for each gateway

### ⚡ Performance
- Multi-threaded checking (5 threads default)
- Real-time progress tracking
- Live statistics: `S` (Success) | `L` (Live) | `D` (Dead) | `I` (Invalid)

### 🔒 Privacy & Security
- Site URLs hidden in logs (displays as `SITE 1`, `SITE 2`, etc.)
- Secure API key management
- Proxy support for anonymity

### 📊 Smart Results
- Color-coded output for easy reading
- Auto-save approved/charged/live/ccn cards
- Telegram forwarder for instant notifications
- Detailed summary after each check

### 🛠️ Easy Configuration
- Simple menu-driven interface
- API key validation
- Custom server support
- Proxy enable/disable

---

## 💰 PRICING

### Public API Keys
| Duration | Price |
|----------|-------|
| 7 Days   | $5    |
| 15 Days  | $10   |
| 30 Days  | $15   |

### Private API - $20/month
**Exclusive benefits:**
- ✅ Dedicated server (faster response)
- ✅ Not listed on status.isnotsin.com
- ✅ Priority support & updates
- ✅ All gateways: Stripe, PPCP, B3
- ✅ BIN checker included
- ✅ Proxy parameter support
- ✅ Perfect for building your own tools

---

## 🎁 DONATION PROGRAM

**Support the project and get rewarded!**

Donate any custom site and receive:
- 🎉 **3 DAYS FREE ACCESS** to Private API
- 🔥 All premium features unlocked
- 💯 Priority support during trial period

*Your donated sites help improve our built-in site pool and benefit the entire community!*

---

## 📦 INSTALLATION

```bash
# Clone the repository
git clone https://github.com/isnotsin/checkmate.git
cd checkmate

# Run the checker
python3 checker.py
```

The script will automatically install required dependencies (`requests`).

---

## 🚀 QUICK START

1. **Configure API Key**
   - Select option `[2]` from menu
   - Enter your API key

2. **Add Sites (Optional)**
   - Select option `[4]` from menu
   - Choose gateway (Stripe/PPCP/B3)
   - Add your custom sites or use built-in sites

3. **Start Checking**
   - Select option `[1]` from menu
   - Choose gateway
   - Select site (Built-in or Custom)
   - Enter card file path
   - Watch the magic happen! ✨

---

## 📁 FILE STRUCTURE

```
checkmate/
├── checker.py          # Main script
├── checker_config.json # Auto-generated config
├── sites/              # Custom site lists
│   ├── stripe.txt
│   ├── ppcp.txt
│   └── b3.txt
└── results/            # Auto-saved results
    ├── approved_*.txt
    ├── charged_*.txt
    ├── live_*.txt
    └── ccn_*.txt
```

---

## 🎨 OUTPUT EXAMPLE

```
09:12:22 : [S] 4602xxxxxxxx1681|04|30|458 | APPROVED - PAYMENT SUCCESS | 1.2.3.4 | STRIPE | SIN-STRIPE
09:12:23 : [L] 5234xxxxxxxx9012|12|28|123 | LIVE - INSUFFICIENT FUNDS | 1.2.3.5 | PPCP | SITE 1
09:12:24 : [D] 4111xxxxxxxx1111|01|25|999 | DEAD - CARD DECLINED | 1.2.3.6 | B3 | SITE 2

PROGRESS: 226/226 | S: 15 | L: 42 | D: 165 | I: 4
```

---

## 📞 CONTACT & SUPPORT

**Owner:** @isnotsin

**Payment Methods:**
- GCash
- Maya
- Binance USDT

**For inquiries:**
- API Keys
- Private API
- Site Donations
- Technical Support

Telegram: [@isnotsin](https://t.me/isnotsin)

---

## ⚠️ DISCLAIMER

This tool is for educational purposes only. The owner is not responsible for any misuse of this software. Always ensure you have permission to test cards and comply with local laws.

---

## 📝 LICENSE

© 2025 @isnotsin - All Rights Reserved

---

**Made with 🔥 by sinno$**