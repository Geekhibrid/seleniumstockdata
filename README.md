# Stock Data Scraper with Selenium

## Overview

This project utilizes Selenium to scrape stock data from Yahoo Finance. The script fetches data such as stock prices, market capitalization, and P/E ratios for a list of specified stock symbols and saves the data into a CSV file. 

## Features

- **Web Scraping with Selenium**: The script automates the browser to extract stock data.
- **Data Storage**: Scraped data is stored in a pandas DataFrame and saved as a CSV file.
- **Error Handling**: The script includes error handling to manage cases where data elements cannot be located.
- **Headless Browser Operation**: Uses Chrome in headless mode for faster execution and no GUI.

## Components

### Libraries Used
- `selenium`: For web scraping and browser automation.
- `pandas`: For data manipulation and storage.
- `time`: For managing request intervals.

### Key Functions
- `get_stock_data(stock_symbol)`: Fetches the stock price, market cap, and P/E ratio for a given stock symbol from Yahoo Finance.
- **Main Execution Flow**: 
  - Initializes the Chrome driver in headless mode.
  - Iterates over a predefined list of stock symbols.
  - Fetches data for each stock symbol and appends it to a list.
  - Converts the list to a pandas DataFrame and checks for any missing data.
  - Saves the DataFrame to a CSV file.
  - Closes the browser.

### Usage
1. **Initialize the Chrome Driver**: Ensure the `chromedriver` is in your PATH.
2. **Define Stock Symbols**: Update the `stock_symbols` list with desired stock symbols.
3. **Run the Script**: Execute the script to fetch the data and save it as a CSV file.

### Error Handling
- The script includes exception handling for scenarios where elements are not found on the Yahoo Finance page, logging errors for each stock symbol if encountered.

## Output
- The final output is a CSV file (`yahoo_finance_data.csv`) containing the stock data for the specified symbols, along with any rows with missing data logged to the console.

## Dependencies
- Selenium: `pip install selenium`
- Pandas: `pip install pandas`
- ChromeDriver: [Download and ensure it is in your PATH](https://sites.google.com/a/chromium.org/chromedriver/)

## Potential Improvements
- **Dynamic Element Handling**: Enhance the script to dynamically locate elements if the structure of Yahoo Finance changes.
- **Multi-threading**: Implement multi-threading to speed up data collection.
- **Extended Data Collection**: Include additional financial metrics as needed.

## Notes
- Ensure that web scraping complies with Yahoo Finance’s terms of service.
- The current script includes a `time.sleep(2)` to prevent hitting the server too quickly; adjust as necessary.

This project serves as a foundational example for web scraping stock data using Selenium and can be extended to include more robust features and error handling mechanisms.
