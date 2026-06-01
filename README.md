# Binance Futures Testnet Trading Bot

A simplified Python trading bot for Binance Futures Testnet (USDT-M) that allows users to place Market, Limit, and Stop-Limit orders through a clean Streamlit-based interface. The application demonstrates API integration, input validation, error handling, and structured project design.

## Features

* Connect securely to Binance Futures Testnet using API credentials
* Place Market Orders (BUY / SELL)
* Place Limit Orders (BUY / SELL)
* Place Stop-Limit Orders (Bonus Feature)
* Input validation for symbol, quantity, price, and order type
* Detailed order response display
* Error handling for API failures and invalid requests
* Logging of requests, responses, and errors
* User-friendly Streamlit interface

---

## Binance Testnet API Credentials

To use the trading bot, you must generate Binance Futures Testnet API credentials.

### Steps to Generate API Keys

1. Visit Binance Futures Testnet:
   https://testnet.binancefuture.com

2. Sign in or create a Testnet account.

3. Navigate to **API Management**.

4. Create a new API Key and Secret Key.

5. Copy and securely store the generated credentials.

### Using API Credentials

When running the application, enter:

* **API Key** → Your Binance Futures Testnet API Key
* **API Secret** → Your Binance Futures Testnet Secret Key

The application uses these credentials to authenticate requests and place orders on the Binance Futures Testnet environment.

### Security Note

* Never commit API Keys or Secret Keys to GitHub.
* Never share your credentials publicly.
* Store credentials securely using environment variables or local configuration files.
* Regenerate your API credentials immediately if they are accidentally exposed.

## Project Structure

```text
Binance-Futures-Testnet-Trading-Bot/
│
├── app.py
├── README.md
├── requirements.txt
├── logs/
│   ├── market_order.log
│   └── limit_order.log
│
└── bot/
    ├── client.py
    ├── orders.py
    ├── validators.py
    └── logging_config.py
```

---

## Prerequisites

* Python 3.8+
* Binance Futures Testnet Account
* Binance Futures Testnet API Key and Secret

Testnet URL:

https://testnet.binancefuture.com

---

## Installation

Clone the repository:

```bash
git clone https://github.com/akhila-3010/Binance-Futures-Testnet-Trading-Bot.git
cd Binance-Futures-Testnet-Trading-Bot
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate the environment:

Windows:

```bash
venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Running the Application

Start the Streamlit application:

```bash
streamlit run app.py
```

The application will open in your browser at:

```text
http://localhost:8501
```

---

## Usage

1. Enter Binance Futures Testnet API Key
2. Enter Binance Futures Testnet Secret Key
3. Select:

   * Symbol (e.g., BTCUSDT)
   * Side (BUY / SELL)
   * Order Type (MARKET / LIMIT / STOP-LIMIT)
4. Enter Quantity
5. Enter Price (required for LIMIT and STOP-LIMIT orders)
6. Submit Order

---

## Sample Order Output

### Market Order

```text
Order Request:
Symbol: BTCUSDT
Side: BUY
Type: MARKET
Quantity: 0.001

Order Response:
Order ID: 123456789
Status: FILLED
Executed Qty: 0.001
```

### Limit Order

```text
Order Request:
Symbol: BTCUSDT
Side: SELL
Type: LIMIT
Quantity: 0.001
Price: 120000

Order Response:
Order ID: 987654321
Status: NEW
Executed Qty: 0.000
```

---

## Logging

Logs are stored in the `logs/` directory and include:

* API requests
* API responses
* Validation errors
* Network failures
* Binance API exceptions

---

## Assumptions

* Users provide valid Binance Futures Testnet credentials.
* Testnet account contains sufficient virtual funds.
* Internet connectivity is available during execution.

---

## Bonus Feature

Implemented Stop-Limit Order support in addition to Market and Limit orders.

---

## Security Considerations

* API credentials are used only for authenticated requests.
* Sensitive credentials should never be committed to GitHub.
* Input validation is performed before order submission.
* Errors are handled gracefully with informative messages.

---

## Technologies Used

* Python 3.x
* Streamlit
* python-binance
* Requests
* Logging

---

## Author

Akhila Chinta
