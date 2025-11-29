# 📱 Receivesms.me Python API Wrapper

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Status: Active](https://img.shields.io/badge/Status-Active-green.svg)](https://receivesms.me)

A lightweight, asynchronous Python wrapper to fetch free temporary phone numbers and SMS verification codes programmatically. This tool interfaces with the fast public nodes of **[Receivesms.me](https://receivesms.me)**.

> **Note:** This tool is for educational purposes and testing. For production use or manual verification, please visit the official website directly.

## 🚀 Features

- **Zero-Delay Fetching:** Get available numbers in < 0.8s.
- **Multi-Country Support:** Access numbers from USA, UK, Vietnam, China, and 40+ countries.
- **Privacy Focused:** No registration or API key required.
- **Async Support:** Built with `aiohttp` for high-performance scraping.

## 📦 Installation

Clone the repository and install dependencies:

git clone https://github.com/your-username/receive-sms-online-api.git
cd receive-sms-online-api
pip install -r requirements.txt
## 💻 Usage Example

Here is a simple example of how to get the latest USA phone numbers:
from receivesms import SMSClientInitialize clientclient = SMSClient()Get list of active countriescountries = client.get_countries()
print(f"Available Countries: {countries}")Get a random US numbernumber = client.get_number(country='US')
print(f"Your Temporary Number: {number}")Watch for incoming SMS (Polling)messages = client.get_messages(number)
for msg in messages:
print(f"From: {msg.sender} | Code: {msg.otp_code}")
## 🌍 Supported Services

You can use these virtual numbers for verifying accounts on:
- Telegram / WhatsApp / Signal
- OpenAI (ChatGPT)
- Google (Gmail) / Facebook / TikTok
- and thousands of other services requiring SMS verification.

## 🔗 Official Source

All data is fetched in real-time from:
**[https://receivesms.me](https://receivesms.me)**  
*(The fastest free SMS receiver service with zero ads)*

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## 📄 License

[MIT](LICENSE)
