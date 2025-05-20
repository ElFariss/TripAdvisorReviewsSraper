# Tripadvisor Reviews Scraper

This project is a Python-based web scraping tool designed to collect user reviews from Tripadvisor attraction pages. It uses **Selenium WebDriver** and **BeautifulSoup** to automate browser interactions and parse the HTML content of the reviews.

## Features

- Automates Firefox browser using Selenium with a custom user-agent.
- Navigates through multiple pages of reviews on a specified Tripadvisor attraction.
- Extracts key review data:
  - Reviewer name
  - Reviewer origin
  - Review title
  - Date and location of visit
  - Star rating
  - Review content
- Saves all collected data to a CSV file (`reviews_scraping.csv`) with proper encoding.

## Requirements

- Python 3.7+
- Firefox browser
- [Geckodriver](https://github.com/mozilla/geckodriver/releases) installed and accessible from `/usr/local/bin/`
- The following Python packages:
  ```bash
  pip install selenium beautifulsoup4 pandas
  ```

## Usage

1. Clone or download this repository.
2. Update the `url` variable in the notebook or script with the target Tripadvisor attraction link.
3. Adjust the sleep time and paths if needed.
4. Run the notebook or script.

Example:
```python
url = "https://www.tripadvisor.co.id/Attraction_Review-g297697-d386919-Reviews-Waterbom_Bali-Kuta_Kuta_District_Bali.html"
```

The script will:
- Launch Firefox.
- Load the specified page.
- Loop through each page of reviews.
- Save the data to `reviews_scraping.csv`.

## Output

A CSV file named `reviews_scraping.csv` containing:
- `author`: Reviewer name
- `asal`: Origin/location of reviewer
- `title`: Title of the review
- `date`: Date of visit
- `location`: Location info from review
- `rating`: Star rating
- `review`: Full review text

## Disclaimer

This project is intended **for educational purposes only**. Web scraping may violate the Terms of Service of the website being scraped. Always review and comply with a website's `robots.txt` and terms before scraping. The authors are not responsible for any misuse of this tool.
