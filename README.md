# CIK Shares Outstanding Dashboard

This single-page web application fetches and displays common stock shares outstanding data for a given company from the SEC EDGAR API.

## Features

*   **Dynamic Data Fetching**: Retrieves `EntityCommonStockSharesOutstanding` data for a specified CIK (Central Index Key).
*   **Max/Min Value Display**: Highlights the maximum and minimum share outstanding values recorded since Fiscal Year 2021.
*   **Responsive Design**: Built with Tailwind CSS for a clean, responsive, and modern user interface.
*   **Dynamic CIK Loading**: The application can load data for different CIKs by appending `?CIK=YOUR_CIK_NUMBER` to the URL (e.g., `index.html?CIK=0001018724`).
*   **Error Handling**: Provides user-friendly error messages if data fetching fails or no qualifying data is found.

## Technologies Used

*   **HTML5**: Structure of the web page.
*   **Tailwind CSS**: Utility-first CSS framework for styling.
*   **JavaScript (ES6+)**: For fetching data, processing, and dynamically updating the DOM.
*   **SEC EDGAR API**: Source of financial data.
*   **AllOrigins Proxy**: Used for cross-origin requests when loading data for a CIK other than the default.

## How to Run

1.  Save the `index.html` file to your local machine.
2.  Open `index.html` in your web browser.

    *   By default, it will display data for **Bank of America (CIK 0000070858)**.
    *   To view data for a different company, append `?CIK=YOUR_CIK_NUMBER` to the URL in your browser's address bar and press Enter (e.g., `file:///path/to/index.html?CIK=0001018724`). The page will update dynamically without a full reload.

## Data Source

Data is sourced from the SEC EDGAR API endpoint:
`https://data.sec.gov/api/xbrl/companyconcept/CIK{CIK}/dei/EntityCommonStockSharesOutstanding.json`

A descriptive `User-Agent` header is used for SEC API requests, as per SEC guidance.
