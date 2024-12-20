## Amazon Product Scraper

This Python script automates the process of searching for products on Amazon India, extracting details of items with discounts greater than 50% from various categories, and saving the data to a CSV file. It uses Selenium WebDriver to interact with the website.

Features

Automated Search: Searches for products in specified categories with discounts over 50%.

Data Extraction: Scrapes detailed information about each product, including:

Product Name

Product Price

Rating

Discount Percentage

Past Details (if available)

Image URL

Shipping Information

Seller Information

CSV Export: Saves all the scraped data into a CSV file for easy analysis.

Prerequisites

Before running the script, ensure the following requirements are met:

Python 3.x: Installed on your system.

Selenium: Install the Selenium library using the following command:

pip install selenium

Chrome Browser: The script uses Chrome for web scraping.

Chromedriver: Download the Chromedriver executable compatible with your Chrome version from here.

Setup

Download Chromedriver:

Place the downloaded chromedriver.exe in a suitable directory.

Update the path variable in the script with the location of your Chromedriver:

path = "C://path_to_chromedriver//chromedriver.exe"

Clone the Repository:

Save the script into a file named amazon_scraper.py.

Install Dependencies:

Install the Selenium library:

pip install selenium

Usage

Run the Script:

Open a terminal or command prompt.

Navigate to the directory containing the script.

Run the script with the following command:

python amazon_scraper.py

Script Workflow:

The script will open Chrome and navigate to Amazon India.

It will search for products in the specified categories with discounts greater than 50%.

Product details will be scraped and saved into a CSV file named amazon_best_sellers.csv.

Output:

The script generates a CSV file containing the following columns:

Category

Product Name

Product Price

Rating

Discount

Past Details

Image URL

Shipped From

Sold By

Configuration

Categories: Modify the categories list in the script to include or exclude categories:

categories = [
    "Smartphones", "Laptops", "Kitchen", "Shoes", "Computers"]

Page Limit: The script currently scrapes the first 10 pages of search results per category. To change this, update the iteration in the scrape_products function.

Error Handling

Missing Data: If certain elements like "Shipped From" or "Sold By" are not found, the script assigns "N/A" to these fields and continues.

Pagination Issues: If there are no more pages to scrape, the script exits the pagination loop gracefully.

Notes

The script is tailored for Amazon India (https://www.amazon.in). If you wish to scrape Amazon in other regions, you may need to update the URL and ensure the XPath selectors match the site structure.

Amazon's website layout may change over time, requiring updates to the XPath selectors in the script.

Disclaimer

This script is intended for educational purposes and personal use only. Scraping websites without permission may violate their terms of service. Always ensure compliance with Amazon's policies and applicable laws.

