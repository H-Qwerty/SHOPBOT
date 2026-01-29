# 🤖 Telegram Shop Bot

A powerful and flexible Telegram shop bot with admin panel, helper roles, product management, and crypto payments integration.

## ✨ Features

### 🛍️ Shopping System
- **Product Catalog** with categories and positions
- **Secure Purchase Flow** with balance system
- **Product Inventory Management**
- **Purchase History** for users
- **FAQ Section** with dynamic placeholders

### 👨‍💼 User Management
- **User Registration** with balance tracking
- **Profile System** showing purchase history
- **Balance Top-up** via Crypto Bot
- **Purchase Receipts** with detailed information

### ⚙️ Admin Panel
- **Full Bot Control** with multiple management options
- **Product Management** (create/edit/delete categories/positions/products)
- **User Management** (search profiles, modify balances)
- **Receipt Management** (view and search all receipts)
- **Statistics Dashboard** with detailed metrics
- **Broadcast System** for announcements

### 👨‍💼 Helper System
- **Helper Roles** with limited permissions
- **Product Management** access
- **Statistics Viewing**
- **Broadcast Capabilities**
- **Maintenance Mode Control**

### 💰 Payment System
- **Crypto Bot Integration** for secure payments
- **Multiple Payment Methods** support
- **Invoice Generation** and status tracking
- **Balance Management** system

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- Telegram Bot Token from [@BotFather](https://t.me/BotFather)
- Crypto Bot Token (optional, for crypto payments)

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/telegram-shop-bot.git
cd telegram-shop-bot
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Configure the bot**
Create a `config.py` file based on `config.example.py`:
```python
# Bot Configuration
BOT_TOKEN = "YOUR_BOT_TOKEN"
ADMIN_IDS = [123456789]  # Your Telegram ID
HELPER_IDS = []  # Optional helper IDs

# Crypto Bot Configuration (optional)
CRYPTO_BOT_TOKEN = "YOUR_CRYPTO_BOT_TOKEN"

# Database Configuration
DATABASE_FILE = "database.json"
```

4. **Run the bot**
```bash
python main.py
```

## 📁 Project Structure

```
telegram-shop-bot/
├── main.py              # Bot entry point
├── config.py            # Configuration file
├── database.py          # Database operations
├── keyboards.py         # All keyboard layouts
├── user_menu.py         # User command handlers
├── admin_panel.py       # Admin command handlers
├── states.py            # FSM states
├── utils.py             # Utility functions
├── database.json        # Data storage (created automatically)
└── requirements.txt     # Dependencies
```

## 🗂️ Database Schema

The bot uses a JSON-based database with the following structure:

```json
{
  "users": {},
  "products": {},
  "categories": {},
  "positions": {},
  "receipts": {},
  "settings": {},
  "stats": {}
}
```

## 🎯 Key Features Explained

### 🔐 Role-Based Access
- **Admins**: Full control over the bot
- **Helpers**: Limited management capabilities
- **Users**: Shopping and profile management

### 📦 Product Management
- **Categories**: Group products logically
- **Positions**: Specific product types
- **Products**: Individual items with unique content
- **Inventory**: Automatic stock tracking

### 💳 Payment Processing
- **Crypto Payments**: Secure cryptocurrency transactions
- **Invoice System**: Track payment status
- **Balance Updates**: Automatic balance management
- **Payment Verification**: Manual/automatic confirmation

### 📊 Statistics
- **User Growth**: Track new users over time
- **Sales Analytics**: Revenue and purchase data
- **Inventory Stats**: Product availability
- **Financial Reports**: Balance and revenue tracking

## 🔧 Advanced Configuration

### Setting Up Crypto Payments

1. Get your Crypto Bot token from [@CryptoBot](https://t.me/CryptoBot)
2. Add it to `config.py`:
```python
CRYPTO_BOT_TOKEN = "your_crypto_bot_token"
```
3. Enable crypto payments in admin panel → Payment Methods

### Customizing FAQs

Use dynamic placeholders in FAQ text:
- `{id}` - User ID
- `{name}` - User's first name
- `{username}` - User's username

### Managing Maintenance Mode

Toggle maintenance mode to temporarily disable purchases while keeping admin access functional.

## 🛡️ Security Features

- **Admin-only commands** with user ID verification
- **Input validation** for all user inputs
- **Safe HTML parsing** for messages
- **Secure payment processing** with Crypto Bot API
- **Database backup** through automatic JSON saving

## 📈 Performance

- **Asynchronous operations** with aiogram
- **Memory-efficient** JSON database
- **Optimized keyboards** with lazy loading
- **Rate limiting** protection
- **Error handling** with detailed logging

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## ⚠️ Disclaimer

This bot is for educational purposes. Ensure compliance with:
- Telegram's Bot Terms of Service
- Local laws regarding e-commerce
- Payment processing regulations
- Data protection laws (GDPR, etc.)

## 🆘 Support

For issues and questions:
1. Check the FAQ in the bot
2. Review the documentation
3. Open a GitHub issue
4. Contact the admin through the bot

## 🌟 Features Roadmap

- [ ] Multi-language support
- [ ] Web dashboard for management
- [ ] Advanced analytics
- [ ] Email notifications
- [ ] API for external integration
- [ ] Affiliate/referral system
- [ ] Discount codes and promotions
- [ ] Automated refunds
- [ ] Product reviews and ratings
- [ ] Shipping address management

---

**Made with ❤️ for the Telegram community**

*This README is dynamically generated and may be updated as the project evolves.*
