# HTTP Widget Scripts
A collection of various scripts for that app HTTP Widget
## HTTP Widget

A lightweight widget for fetching and formatting cryptocurrency prices from public APIs like CoinGecko. 

### Features

- Fetch live crypto prices (e.g., XRP, Monero) in USD.
- Extract values using key paths, regex, or custom JavaScript.
- Auto-refresh with configurable intervals.
- Supports notifications based on extracted values.

### Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/httpwidget.git
cd httpwidget

Open in your preferred environment and configure your widgets JSON files.

Usage
	1.	Configure your widget JSON with:
	•	url for the API endpoint.
	•	extractByKeyPath or extractByJavaScript to parse the response.
	•	Optional autoTriggerInterval for periodic updates.
	2.	Load the widget in the app.
	3.	View live prices and formatted outputs.

Example JSON

{
  "alias": "💰 XRP",
  "url": "https://api.coingecko.com/api/v3/simple/price?ids=monero&vs_currencies=usd",
  "extractByJavaScript": "let json = JSON.parse(responseString);\nlet xrpPrice = json.monero.usd;\nreturn `$${xrpPrice.toFixed(2)}`;",
  "autoTriggerInterval": 300
}

Contribution
	•	Add new cryptocurrency endpoints.
	•	Improve extraction methods.
	•	Enhance notifications or formatting options.

License

MIT License. No PII is stored in this repository; all data comes from public APIs.