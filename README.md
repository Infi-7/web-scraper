# Web Scraper

A simple and efficient Python-based web scraping script designed to extract and store data from websites. This project uses the `requests` library to fetch HTML content, `BeautifulSoup` for parsing, and the `csv` module to save data into a structured file format.

## Features
- Fetches website content via an environment-specified URL.
- Parses HTML to extract specific data enclosed in `<strong>` tags.
- Processes and cleans the extracted data.
- Avoids duplicate entries in the output CSV file.
- Saves the scraped data to a CSV file (`top_100_games.csv`).

## Technologies Used
- **Python 3.8+**
- **Libraries:**
  - `requests`: To fetch web content.
  - `beautifulsoup4`: To parse and extract data from HTML.
  - `python-dotenv`: To manage environment variables.
  - `csv`: To handle CSV file creation and updates.

## Prerequisites
- Python 3.8 or higher installed on your system.
- Required Python libraries installed:
  ```bash
  pip install -r requirements.txt
  ```
- A `.env` file containing the following variable:
  ```env
  site_link=<URL_OF_WEBSITE>
  ```

## Installation and Setup
1. Clone this repository:
   ```bash
   git clone https://github.com/Infi-7/web-scraper.git
   cd web-scraper
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Create a `.env` file in the root directory and add your target website link:
   ```env
   site_link=https://example.com
   ```

4. Run the script:
   ```bash
   python scraper.py
   ```

## Output
- The script generates a CSV file named `top_100_games.csv` in the project directory.
- Each row in the CSV contains one cleaned data entry scraped from the website.

## Error Handling
- **Missing Environment Variable:** The script raises an error if `site_link` is not defined in the `.env` file.
- **Network Errors:** Handles errors like connection timeouts and invalid URLs gracefully.
- **Duplicate Data:** Ensures that no duplicate entries are appended to the CSV file.

## Contributing
Contributions are welcome! Follow these steps to contribute:
1. Fork this repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a pull request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

### Notes
- Ensure the target website allows scraping. Refer to the website's `robots.txt` file and terms of service.
- Modify the HTML parsing logic in the script if the structure of your target website differs.
