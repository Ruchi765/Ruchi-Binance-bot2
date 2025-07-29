# Binance Futures Order Bot

## 📌 Project Overview
This project is a **CLI-based trading bot** for Binance USDT-Margined Futures built with Python. It supports placing both **basic and advanced order types** via command-line interface.
It demonstrates real-world usage of the Binance Futures API, proper input validation, structured logging, and good coding practices through modular files.
The bot is structured for reliability, reusability, and extendability.

## ✅ Features
🔹 Core Orders (Mandatory)
- Market Order
- Limit Order

🔹 Advanced Orders (Bonus)
- Stop-Limit Order
- OCO (One Cancels the Other)
- TWAP (Time-Weighted Average Price)
- Grid Strategy (Buy low/sell high within price range)

🔹 Additional
- Input Validation
- Structured Logging (`bot.log`)
- .env-based API key security
- Clean project structure

 🧾 File Structure
Ruchi_binance_bot/
│
├── src/
│ ├── market_orders.py
│ ├── limit_orders.py
│ └── advanced/
│ ├── stop_limit.py
│ ├── oco.py
│ ├── twap.py
│ └── grid_strategy.py
│
├── .env # API keys (not to upload to GitHub)
├── bot.log # Logs of order execution and errors
├── README.md # This file
├── report.pdf # Screenshots and explanations
├── requirements.txt # Dependency file

---
🔐 API Setup

Create a `.env` file in the root directory and add your Binance API keys like this:
API_KEY=your_binance_api_key
API_SECRET=your_binance_api_secret

## ⚙️ Installation
1. Clone the repository:
```bash
git clone https://github.com/YOUR_USERNAME/yourname-binance-bot.git
cd yourname-binance-bot
Create a virtual environment and activate it:
python -m venv venv
venv\Scripts\activate  # Windows
source venv/bin/activate  # Mac/Linux
Install required libraries:
pip install -r requirements.txt
🚀 How to Use
✅ Market Order
bash
Copy
Edit
python src/market_orders.py BTCUSDT BUY 0.01
✅ Limit Order
bash
Copy
Edit
python src/limit_orders.py BTCUSDT SELL 0.01 30000
🛑 Stop-Limit Order
bash
Copy
Edit
python src/advanced/stop_limit.py BTCUSDT BUY 0.01 29900 29800
🔁 OCO Order
bash
Copy
Edit
python src/advanced/oco.py BTCUSDT BUY 0.01 31000 29500
⏱️ TWAP (Time-Weighted Average Price)
bash
Copy
Edit
python src/advanced/twap.py BTCUSDT BUY 0.05 5 60
📉 Grid Strategy
bash
Copy
Edit
python src/advanced/grid_strategy.py BTCUSDT 29000 31000 10 0.005
📝 Logging
All actions and errors are stored in bot.log. Each entry contains:

Timestamp

Order type

Response or error message

Example:

pgsql
Copy
Edit
2025-07-29 10:32:12 INFO Market order placed: BTCUSDT BUY 0.01
2025-07-29 10:32:13 ERROR Invalid price for limit order
📦 Dependencies
Installed using:

bash
Copy
Edit
pip install -r requirements.txt
Contents of requirements.txt:

Copy
Edit
python-binance
python-dotenv
requests
pandas
schedule
📄 Report
Located in report.pdf

Contains:

Screenshots of working CLI output

Brief explanation of logic

Error handling examples

Challenges and learnings

📥 Submission Checklist (As per Instructor)
✅ Market and Limit orders
✅ At least 2 advanced orders (Stop-Limit, OCO, TWAP, Grid)
✅ Structured bot.log
✅ .zip structure matches instructor format
✅ Private GitHub repository
✅ Instructor added as collaborator
✅ report.pdf and README.md included

👨‍💻 Author
Name: Ruchi Tiwari
GitHub: Ruchi765
Instructor: [instructor_ruchi]

