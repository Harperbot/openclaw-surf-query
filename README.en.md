# 🏄 openclaw-surf-query

[繁體中文](README.md) | English

A Taiwan surf spot query OpenClaw Skill. Search for surf spots via Telegram, LINE, or iMessage and get real-time tides, wind conditions, typhoon dynamics, sunrise times, and one-click navigation links.

**🔥 What's new:**
* 🚀 **Native OpenClaw Plugin Support**: Added `openclaw.plugin.json`. You can now install it directly via ClawHub and manage your API Key without manually editing config files.
* ✨ **Markdown Output Optimization**: Upgraded lengthy URLs to clean Markdown Inline Links (e.g., `[🍎 Apple Maps Nav]`).

## Features

- **30 Surf Spots Database**: Covers North, Northeast, East, South, and West Taiwan.
- **Multiple Query Methods**: Search by spot name, region name, or GPS coordinates (within 30km).
- **Real-time Tides & Wind**: Real-time data from Taiwan's Central Weather Administration (CWA). Automatically determines if the wind is offshore (good waves).
- **Typhoon Dynamics**: Shows active typhoons within 2000km of Taiwan.
- **Sunrise/Sunset**: Calculated accurately using astronomical formulas based on the spot's coordinates.
- **Parking Query Integration**: Optional. Works with the [parking_query](https://github.com/Harperbot/openclaw-parking-query) skill.

## Prerequisites

### 1. OpenClaw
Please install and configure [OpenClaw](https://github.com/openclaw/openclaw) first.

### 2. CWA API Key (Free)
Register an account at [opendata.cwa.gov.tw](https://opendata.cwa.gov.tw) to get your authorization code.
> The skill can still run without it, but real-time tides, wind, and typhoon data will be omitted.

### 3. Python Packages
```bash
pip3 install requests
```

## Installation

### Method 1: Via ClawHub (Recommended)
```bash
clawhub install openclaw-surf-query
```
After installation, go to the Plugins page in the OpenClaw Control UI and enter your `CWA_API_KEY` (format: `CWA-your_auth_code`).

### Method 2: Manual Installation
```bash
# 1. Clone into your OpenClaw skills directory
git clone https://github.com/Harperbot/openclaw-surf-query.git ~/.openclaw/skills/surf_query

# 2. Set your CWA_API_KEY via CLI or the Web UI

# 3. Restart the gateway
openclaw gateway restart
```

## License
MIT