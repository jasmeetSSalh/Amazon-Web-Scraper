# Amazon Web Scraper

This project is a simple web scraper designed to extract product information from an Amazon product page, monitor changes in the product's price over time, and store the collected data in a CSV file. The script utilizes Python and popular libraries such as BeautifulSoup for web scraping and Pandas for data manipulation.

## Features:

1. **Web Scraping:** The script connects to a specified Amazon product page using a user-agent to mimic a browser. It then extracts relevant information such as the product title and price using BeautifulSoup.

2. **Data Cleanup:** After retrieving the data, the script cleans up the extracted information by removing unnecessary whitespaces and characters.

3. **Timestamping:** The current date is added as a timestamp to track when the data was collected.

4. **CSV File Handling:** The script creates a CSV file named 'AmazonWebScraperDataset.csv' and writes the headers ('Title', 'Price', 'Date') along with the collected data into the file. Subsequent runs of the script append new data to the existing CSV file.

5. **Automation:** The main functionality is encapsulated within a function called `check_price()`, which can be executed at regular intervals. The script includes a loop that runs the `check_price()` function at a set time interval (every 24 hours in this case) and sleeps in between.

6. **Email Notification (Optional):** The script includes an optional function `send_mail()` that can be used to send an email notification if the product's price falls below a specified threshold. This feature uses the smtplib library to send emails.

## Usage:

1. Clone the repository to your local machine.
   
2. Install the required libraries using the following command:

pip install beautifulsoup4 requests pandas


3. Set up your own Amazon product URL in the `URL` variable within the `check_price()` function.

4. Optionally, configure the email notification by providing your Gmail credentials and adjusting the threshold in the `send_mail()` function.

5. Run the script, and it will start scraping data, updating the CSV file, and checking the price at regular intervals.

Notes: this project is intended to be used only for learning purposes

