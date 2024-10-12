# Currency Converter Application

A simple currency converter web application that uses the [Currency API by Fawaz Ahmed](https://github.com/fawazahmed0/currency-api). The app fetches real-time exchange rates and displays the conversion results between two selected currencies.

## Features

- **Real-time exchange rates**: Uses the Currency API to get the latest exchange rates.
- **Dropdown for currency selection**: Allows users to choose currencies from a dropdown menu.
- **Automatic currency flag updates**: Displays flags of selected currencies dynamically.
- **Fallback mechanism**: Shows an error message if the exchange rate cannot be fetched.
  ---
  ![image](https://github.com/user-attachments/assets/196dec6f-5bf6-43cc-b990-3287b87d83a1)

  ---

## API Change Notice

This project has been updated to comply with recent changes to the Currency API:
- The base URL has changed from `https://cdn.jsdelivr.net/gh/fawazahmed0/currency-api@1/{date}/{endpoint}` to `https://cdn.jsdelivr.net/npm/@fawazahmed0/currency-api@{date}/v1/{endpoint}`.
- The endpoint `/currencies/{currencyCode}/{currencyCode}` is no longer supported. Instead, the endpoint `/currencies/{currencyCode}` should be used.
- The exchange rate is now fetched from the new structure and accessed as follows:
  ```javascript
  const URL = `/currencies/{fromCurrency}.json`;
  rate = json[fromCurrency][toCurrency];

Installation and Usage
----------------------

### Prerequisites

-   Basic knowledge of HTML, CSS, and JavaScript.
-   An active internet connection to fetch currency rates from the API.

### Getting Started

1.  Clone this repository:

    bash

    Copy code

    `git clone https://github.com/yourusername/currency-converter.git`

2.  Open `index.html` in your browser:

    bash

    Copy code

    `open index.html`

3.  Select the currencies and enter the amount to convert.

### Fallback Mechanism

In case of API failure, the app will show the following message:

arduino

Copy code

`"Unable to fetch exchange rate. Please try again later."`

### Example

If you select `USD` as the "From" currency and `INR` as the "To" currency, and input `100` in the amount field, the app will display the exchange rate and calculate the result as:

css

Copy code

`100 USD = [calculated amount] INR`

Code Overview
-------------

### Key JavaScript Functions

-   **updateExchangeRate**: Fetches the latest exchange rate from the API and updates the result.
-   **updateFlag**: Updates the country flag for the selected currency using the [Flags API](https://flagsapi.com/).

### Currency API

-   The app fetches exchange rates from the URL:

    bash

    Copy code

    `https://cdn.jsdelivr.net/npm/@fawazahmed0/currency-api@latest/v1/currencies/{fromCurrency}.json`

### Fallback

-   The app implements a basic error-handling mechanism that displays an error message in case of API failure.

License
-------

This project is open-source and available under the MIT License.

Acknowledgments
---------------

-   Currency data powered by [Fawaz Ahmed's Currency API](https://github.com/fawazahmed0/currency-api).
-   Country flags provided by [Flags API](https://flagsapi.com/).
# View Site [click here](https://oviyan007.github.io/CurrencyConveter/)
