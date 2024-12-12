# Recycle Me - Web Scraping and Discount Calculation Scripts

## Overview
This repository contains Python scripts for the **Recycle Me** project that facilitate web scraping and discount calculation. The code extracts product details from the SAS supermarket website and calculates discounts for products nearing their expiration dates.

---

## Features

### 1. Web Scraping
- **Library Dependencies**: Uses `BeautifulSoup` and `requests` to scrape product information.
- **Extracted Data**:
  - Product name
  - Price
  - Product code
  - Availability
  - Image URL (if available)

### 2. Discount Calculation
- Calculates remaining shelf life and applies a 30% discount for products with less than 20% of their shelf life remaining.
- Displays products with their original price, remaining percentage, and discounted price.

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your_username/your_repository.git
   ```
2. Navigate to the project directory:
   ```bash
   cd your_repository
   ```
3. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

---

## Usage

### Web Scraping Scripts
#### File: `web_scraping.py`
1. Define the URL of the page to scrape:
   ```python
   url = "https://www.sas.am/catalog/molochnye_produkty/"
   ```
2. Run the script to scrape product details:
   ```bash
   python web_scraping.py
   ```
3. Outputs:
   - Scraped product details are printed in the console.
   - Optionally saves the data to a CSV file.

#### Example Output:
```plaintext
Page content fetched successfully.
Product slider found.
Found 10 products.
Scraped Products:
{'Ապրանքի անվանում': 'Milk', 'Գին': 450, 'Ապրանքի կոդ': '12345', 'Հասանելիություն': 'Available'}
```

### Discount Calculation Script
#### File: `discount_calculation.py`
1. Customize the `products` list with relevant product data:
   ```python
   products = [
       {"name": "Product A", "production_date": "2024-01-01", "expiration_date": "2024-12-31", "price": 100},
       ...
   ]
   ```
2. Run the script to calculate discounts:
   ```bash
   python discount_calculation.py
   ```
3. Outputs:
   - A tabular display of products with discounts applied.

#### Example Output:
```plaintext
Name           Production Date Expiration Date Price     Remaining % Discounted Price
Product A      2024-01-01      2024-12-31      100       75.00       100.00
Product D      2023-12-01      2024-05-01      80        5.00        56.00
```

---

## File Descriptions

- **`web_scraping.py`**: Script for scraping product details from SAS supermarket.
- **`discount_calculation.py`**: Script to calculate discounts based on shelf life.
- **`requirements.txt`**: List of Python dependencies for the project.

---

## Challenges
- Handling dynamic website elements not directly accessible with `BeautifulSoup`.
- Managing missing or incomplete product data (e.g., missing prices or availability).
- Parsing and formatting inconsistent product price representations.

---

## Future Improvements
- Automate scraping for multiple pages of the website.
- Use advanced tools like `selenium` or `playwright` for dynamic content extraction.
- Integrate real-time discount calculation into the app's backend.

---

## Contributing
Contributions are welcome! Please fork this repository and create a pull request with your improvements.

---

## License
This project is licensed under the MIT License. See `LICENSE` for details.

---

# RecycleMe
