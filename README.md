A Python-based Command Line Interface (CLI) application to track cryptocurrency investments using real-time market data, local persistence, and automation-friendly design.

This project demonstrates API integration, database handling, and CLI tooling, making it suitable for backend, DevOps, and automation-focused roles.

Features

Fetch live cryptocurrency prices using CoinGecko API

Store buy/sell transactions locally using SQLite

Calculate net holdings and portfolio value

Import investment data from CSV files

Export portfolio data to CSV

Clean and modular CLI commands using Click

Tech Stack

Language: Python

CLI Framework: Click

Database: SQLite

API: CoinGecko Public API

Data Format: CSV

Concepts: REST APIs, SQL, CLI design, automation scripting

📂 Project Structure
crypto-portfolio-tracker/
│
├── README.md
├── .gitignore
├── main.py
├── portfoli.db
├── crypto_traders.csv


Installation
Clone the repository
git clone git@github.com:me-thakur/investment_portfolio.git


CLI Commands
Show live coin price
python main.py show-coin-price --coin_id bitcoin --currency usd

Add investment (Buy)
python main.py add-investment --coin_id bitcoin --currency usd --amount 0.5

Add investment (Sell)
python main.pyadd-investment --coin_id bitcoin --currency usd --amount 0.1 --sell

Get portfolio value
python main.py get-investment-value --coin_id bitcoin --currency usd

Import investments from CSV
python main.py import-investment --csv_file sample_data/investments_sample.csv

Export investments to CSV
python main.py export-investment --export_file portfolio_export.csv

Sample CSV Format
coin_id,currency,amount,sell,date
bitcoin,usd,0.5,0,2024-01-10 10:30:00
bitcoin,usd,0.1,1,2024-02-01 14:20:00

Architecture Overview
CLI (Click)
   │
   ├── API Layer (CoinGecko)
   │
   └── Database Layer (SQLite)


CLI Layer: User interaction & command parsing

API Layer: External price retrieval

Database Layer: Persistent investment storage

Notes & Limitations

Uses CoinGecko public API (rate limits apply)

SQLite database is local and lightweight

No authentication required

Future Enhancements

Add error handling & retries

Add logging

Dockerize the application


Author

Vivek Kumar
Tech Support Analyst → DevOps / Backend Engineering
LinkedIn: https://www.linkedin.com/in/methakur
GitHub: https://github.com/me-thakur
