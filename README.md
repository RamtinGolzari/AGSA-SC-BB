# AGSA Status Bot for Bale Messenger 🤖

A powerful and efficient PHP bot that monitors AG-SA player status and delivers real-time notifications through Bale messenger. Perfect for gaming communities who want to track player statuses automatically.

![Bale Bot](https://img.shields.io/badge/Bale-Bot-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![PHP Version](https://img.shields.io/badge/PHP-%3E%3D7.4-purple)

## ✨ Features

- 🔄 Real-time status monitoring
- 🔔 Instant notifications on status changes
- 📊 Status image visualization
- 👥 Multi-user subscription system
- 🛡️ Robust error handling
- 📝 Detailed logging system

## 🚀 Getting Started

### Prerequisites

- PHP 7.4 or higher
- cPanel hosting or any PHP web hosting
- GD Library enabled in PHP
- Bale Bot Token (get from @BotFather on Bale)

### Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/agsa-status-bot.git
```

2. Upload files to your web hosting
```
├── config.php
├── functions.php
├── webhook.php
├── check_status.php
└── README.md
```

3. Create necessary files with proper permissions
```bash
touch subscribers.json last_status.txt bot_log.txt
chmod 666 subscribers.json last_status.txt bot_log.txt
```

4. Configure your bot
- Edit `config.php` with your settings:
```php
define('BOT_TOKEN', 'YOUR_BALE_BOT_TOKEN');
define('ACCOUNT_NAME', 'YOUR_ACCOUNT_NAME');
```

5. Set up webhook
```
https://api.bale.ai/bot{BOT_TOKEN}/setWebhook?url=https://your-domain.com/path-to/webhook.php
```

6. Add cron job in cPanel
```bash
* * * * * php /home/username/public_html/path-to/check_status.php
```

## 🎮 Usage

### Bot Commands
- `/start` - Subscribe to status updates
- `/stop` - Unsubscribe from updates
- `/status` - Check current status
- `/help` - Show help message

### Status Indicators
- 🟢 Online
- 🟠 Sleep
- 🔴 Offline

## 🛠️ Technical Details

The bot uses:
- PHP GD library for image processing
- Bale.ai Bot API for messaging
- File-based storage for subscribers and status
- Cron job for automated monitoring

## 📝 Logging

The bot maintains detailed logs in `bot_log.txt`:
- Status checks
- API responses
- Subscriber management
- Error tracking

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📜 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Special thanks to [Ramtin](https://github.com/RamtinGolzari) for the original concept
- AG-SA community for inspiration
- Bale messenger platform for the API

## 📞 Support

If you have any questions or need help, feel free to:
- Open an issue
- Contact via [Telegram](https://t.me/mixtrus)
- Email: themixtrus@gmail.com

---

Made with ❤️ for the AG-SA Community
