# Card Checker Tool

Multi-gateway card checker with Stripe, PPCP, and B3 support.

## Installation

### Method 1: Using Installer (Recommended)

```bash
# Download installer
curl -O https://raw.githubusercontent.com/isnotsin/checkmate/main/app.py

# Run installer
python app.py
# Choose [1] Install Checker
```

### Method 2: Direct Clone

```bash
git clone https://github.com/isnotsin/checkmate.git
cd checkmate
python checker.py
```

## Usage

### First Time Setup

1. Run the checker:
```bash
python checker.py
```

2. Configure API Key (Menu [2])
```
Enter your API key from bot
```

3. (Optional) Configure Telegram Forwarder (Menu [6])
```
Bot Token: your_bot_token
Chat ID: your_chat_id
```

4. Start checking (Menu [1])

## Features

- ✅ Multi-gateway support (Stripe, PPCP, B3)
- ✅ Progress counter
- ✅ Telegram notifications
- ✅ API key validation
- ✅ Proxy support
- ✅ Results auto-save

## Directory Structure

```
checkmate/
├── checker.py          # Main script
├── sites/              # Gateway sites
│   ├── stripe.txt
│   ├── ppcp.txt
│   └── b3.txt
└── results/            # Check results
    ├── approved_*.txt
    ├── charged_*.txt
    ├── ccn_*.txt
    └── live_*.txt
```

## Configuration

Config saved in `checker_config.json`:

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

## Adding Sites

Edit files in `sites/` directory:

```bash
# Stripe sites
echo "newsite.com" >> sites/stripe.txt

# PPCP sites
echo "shop.example.com" >> sites/ppcp.txt

# B3 sites
echo "btsite.com" >> sites/b3.txt
```

Or use Menu [4] in checker.

## Updating

### Using Installer:
```bash
python app.py
# Choose [2] Update Checker
```

### Manual:
```bash
cd checkmate
git pull
```

## Requirements

- Python 3.6+
- requests module (auto-installed)

## Support

Telegram: @isnotsin