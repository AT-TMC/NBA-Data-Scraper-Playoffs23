# NBA-Data-Scraper-Playoffs23

This python script collects and manipulates data related to NBA matches and player performances from [Hashtag Basketball](https://hashtagbasketball.com/). The final output is a CSV file that contains combined data from NBA schedule grid and Fantasy basketball rankings that can be used to project fantasy playoff performance.

## Prerequisites

Before you begin, ensure you have met the following requirements:
* Python 3.x installed
* Selenium library installed in Python
* BeautifulSoup library installed in Python
* Pandas library installed in Python
* Google Chrome browser installed (required for Selenium)
* Chrome WebDriver downloaded and placed in the specified path

## Functionality

Here's what the script does:
* It opens two different web pages on Hashtag Basketball using Selenium and Chrome WebDriver:
    1. [Advanced NBA Schedule Grid](https://hashtagbasketball.com/advanced-nba-schedule-grid)
    2. [Fantasy Basketball Rankings](https://hashtagbasketball.com/fantasy-basketball-rankings)
* It navigates through these pages, clicks on buttons to load data, and scrapes tables using BeautifulSoup.
* It collects and processes the data using Pandas, and then merges the data from both pages.
* It exports the final dataframe as a CSV file named 'FantasyPlayoffsTop300.csv'.

## Usage

```python
python nba_data_scraper.py
```

After running the script, check the directory where the script is located for the generated CSV file.

Please ensure that the correct file path for the Chrome WebDriver is provided in the script.

```python
PATH = "C:\FILE PATH OF YOUR WEBDRIVER\chromedriver.exe"
```

## Output

The script generates a CSV file with the following columns:
* Player Name
* Team
* Weekly Games Scheduled
* Player Stats for last 30 days
* Total Games for 3 weeks

## Known Issues

The script is dependent on the structure of the webpages it scrapes. If the website changes its layout or the names of its HTML elements, the script may stop working.

## Future Improvements

* Implement error handling for webpage structure changes.
* Automate the download and setup of Chrome WebDriver.
* Include command line arguments for customizable data scraping.

## License

This project is licensed under the terms of the [MIT license](https://opensource.org/licenses/MIT).

## Project Status

This project is currently being maintained and improved based on user feedback. If you have suggestions, please feel free to create an issue or pull request.
