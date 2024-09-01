# Stock Exchange Web Scraping

Web scraping stock exchanges for multiple purposes

## Indonesia Stock Exchange

The purpose of scraping this was to categorise the announcements in idx.co.id to different financial events and create a template from their PDFs content for the company to ingest in their system as validation. This decrease the time to validate by 65%.

How it works is by filtering the announcements by the given keywords and downloading specific PDF where the title contains certain keywords. Then we will read the PDFs and convert some, issued capital and meetings, to a table format where it will be further formatted to fit a specific template. SQL is used to match the internal company identifier with the company's listing ID in the stock exchange.

* The keywords to use to categorise and also ignore is from an Excel file to enable users to easily adjust the categories.
* The reason why we need to download using selenium and pyAutoGUI is the company's security limitation, it doesn't let them download files in the background.
* PDF reader function for meetings not included here

## Swiss Stock Exchange

The purpose of scraping the Swiss Stock Exchange was to get a list of companies listed and their issued capital amount at the time of being scraped. This decrease the time for validation by 90% and increase accuracy and timeliness of the company's database by 70%.