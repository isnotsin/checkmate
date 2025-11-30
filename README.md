# CHECKMATE - Multi-Gateway Card Checker

```
░▄▀▀░█▄█▒██▀░▄▀▀░█▄▀░█▄▒▄█▒▄▀▄░▀█▀▒██▀
░▀▄▄▒█▒█░█▄▄░▀▄▄░█▒█░█▒▀▒█░█▀█░▒█▒░█▄▄
         @isnotsin
```

Professional card checker with Stripe, PPCP, and Braintree B3 support.

## Features

- ✅ **Multi-Gateway Support** - Stripe, PPCP, B3 (more coming soon)
- ✅ **Smart Card Parser** - Extracts cards from ANY format
- ✅ **Progress Counter** - Real-time checking progress
- ✅ **Telegram Forwarder** - Personal hit notifications
- ✅ **API Key System** - Secure authentication
- ✅ **Proxy Support** - Enable/disable anytime
- ✅ **Auto-Save Results** - Organized in results folder
- ✅ **Per-Gateway Sites** - Separate site lists
- ✅ **Config Persistence** - All settings saved

## Installation

### Quick Install (Recommended)

```bash
git clone https://github.com/isnotsin/checkmate.git
cd checkmate
python checker.py
```

### Using Installer

```bash
curl -O https://raw.githubusercontent.com/isnotsin/checkmate/main/app.py
python app.py
# [1] Install Checker
# [3] Run Checker
```

## First Time Setup

1. **Get API Key**
   - Contact [@isnotsin](https://t.me/isnotsin) on Telegram
   - Choose your plan (see pricing below)

2. **Run Checker**
   ```bash
   python checker.py
   ```

3. **Configure API Key** (Menu [2])
   ```
   Enter your API key
   ```

4. **Optional: Setup Telegram Forwarder** (Menu [6])
   ```
   Bot Token: your_bot_token
   Chat ID: your_chat_id
   ```

5. **Start Checking!** (Menu [1])

## Usage

### Main Menu

```
[1] START CHECKER
[2] CONFIGURE API KEY
[3] CONFIGURE SERVER
[4] CONFIGURE SITES
[5] CONFIGURE PROXY
[6] CONFIGURE FORWARDER
[7] BUY API KEY
[8] EXIT
```

### Checking Cards

1. Select gateway (Stripe/PPCP/B3)
2. Enter card files (comma separated)
3. Watch real-time results with progress counter

### Card File Format

The checker is **smart** and handles ANY format:

```
✅ 4111111111111111|12|28|123
✅ CARDS|4111111111111111|12|28|123
✅ CARDS -> 4111111111111111 | 12 | 28 | 123
✅ 4111-1111-1111-1111/12/2028/123
✅ Random text 4111111111111111 12 28 123
```

Just throw your cards in a text file and it will extract them automatically!

## Directory Structure

```
checkmate/
├── checker.py              # Main checker
├── checker_config.json     # Your settings
├── sites/                  # Gateway sites
│   ├── stripe.txt
│   ├── ppcp.txt
│   └── b3.txt
└── results/                # Check results
    ├── approved_*.txt
    ├── charged_*.txt
    ├── ccn_*.txt
    └── live_*.txt
```

## Configuration

All settings are saved in `checker_config.json`:

```json
{
  "api_key": "YOUR_KEY",
  "api_base": "https://ey-pi-ay.onrender.com",
  "bot_token": "",
  "chat_id": "",
  "proxy": "",
  "proxy_enabled": false
}
```

## Managing Sites

### Option 1: Edit Text Files
```bash
# Add Stripe site
echo "newsite.com" >> sites/stripe.txt

# Add PPCP site
echo "shop.example.com" >> sites/ppcp.txt

# Add B3 site
echo "btsite.com" >> sites/b3.txt
```

### Option 2: Use Menu [4]
- Select gateway
- Add/remove sites

## API Key Pricing

### Public API Keys
- **$5** → 7 Days
- **$10** → 15 Days  
- **$15** → 30 Days

### Private API - $20/Month
Exclusive features:
- ✓ Dedicated server (faster response)
- ✓ Not listed on status.isnotsin.com
- ✓ Priority support & updates
- ✓ All gateways: Stripe, PPCP, B3
- ✓ BIN checker included
- ✓ Proxy support
- ✓ Perfect for building your own tools
- ✓ New gateways added regularly

**Contact:** [@isnotsin](https://t.me/isnotsin)  
**Payment:** Crypto/PayPal

## Features Breakdown

### Smart Card Parser
Automatically extracts cards from any format:
- Handles separators: `|`, `-`, `/`, spaces
- Converts 4-digit years to 2-digit (2028 → 28)
- Auto-pads months (9 → 09)
- Finds cards anywhere in text

### Progress Counter
```
11:45:23 : [1/100] [S] 4242...4242 | SUCCEEDED - CARD ADDED | 123.45.67.89 | STRIPE
11:45:28 : [2/100] [L] 4111...1111 | INCORRECT_CVC - CVV INVALID | 123.45.67.89 | STRIPE
```

### Result Statuses
- **[S]** Success (Approved/Charged) - Green
- **[L]** Live (CCN Matched/3DS) - Orange
- **[D]** Dead (Declined) - Red
- **[I]** Invalid (Error/Timeout) - Gray

### Auto-Save Results
Results saved in `results/` folder:
- `approved_TIMESTAMP.txt`
- `charged_TIMESTAMP.txt`
- `ccn_TIMESTAMP.txt`
- `live_TIMESTAMP.txt`

### Telegram Notifications
Get instant notifications for:
- ✅ Approved cards
- 💰 Charged cards
- 🟢 CCN matched cards
- ✅ Live cards

## Updating

### Using Git
```bash
cd checkmate
git pull
```

### Using Installer
```bash
python app.py
# [2] Update Checker
```

## Requirements

- Python 3.6+
- requests (auto-installed)

## Advanced Usage

### Using Proxy
1. Menu [5] - Configure Proxy
2. Set proxy URL
3. Enable/disable anytime
4. Proxy persists across sessions

### Custom API Server
1. Menu [3] - Configure Server
2. Enter custom API base URL
3. Or reset to default

### Multiple Card Files
```bash
# When prompted for files:
cards1.txt, cards2.txt, cards3.txt
```

## Troubleshooting

### API Key Expired
- Checker auto-detects expired keys
- Get new key from [@isnotsin](https://t.me/isnotsin)

### Cards Not Loading
- Check file exists
- Ensure cards are in supported format
- Smart parser handles most formats

### Connection Issues
- Check internet connection
- Verify API server status
- Try disabling proxy if enabled

## Support

- **Telegram:** [@isnotsin](https://t.me/isnotsin)
- **Issues:** GitHub Issues
- **Updates:** Follow on Telegram

## Credits

Developed by [@isnotsin](https://t.me/isnotsin)

---

**Note:** This tool is for educational purposes. Use responsibly and legally.