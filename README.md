# Web Scraper for Cardamom Prices
![Project Banner](public/project_image_cardamom.jpeg)

This Python script scrapes daily domestic price data for small and large cardamom from the official Indian Spices Board website and saves it as CSV files. The script is scheduled to run every day at 8:00 AM automatically.

## Features
- Scrapes data for **Small Cardamom** and **Large Cardamom**.
- Extracts important details such as date, auctioneer, quantity, and price.
- Saves data into CSV files for further analysis.
- Automatically runs daily at a specified time using a scheduler.

## Prerequisites
Ensure you have Python installed (version 3.6 or higher). You also need the following Python libraries:

- `requests` (for sending HTTP requests)
- `beautifulsoup4` (for parsing HTML content)
- `csv` (for saving data in CSV format)
- `schedule` (for scheduling the script to run automatically)

To install the required dependencies, run:
```sh
pip install requests beautifulsoup4 schedule
```

## How to Use
### Step 1: Clone or Download the Repository
```sh
git clone https://github.com/yourusername/cardamom-price-scraper.git
cd cardamom-price-scraper
```

### Step 2: Run the Script Manually (Optional)
If you want to run the script manually instead of waiting for the scheduled execution:
```sh
jupyter notebook Project.ipynb
```

### Step 3: Schedule the Script to Run Automatically
The script is already set up to run daily at 8:00 AM. Simply keep the notebook running in the background.
```sh
jupyter notebook Project.ipynb
```

### Step 4: Check for Output
After execution, CSV files will be generated with the format:
- `small_cardamom_prices_YYYYMMDD.csv`
- `large_cardamom_prices_YYYYMMDD.csv`

Each file will contain extracted price data for that day.

## Scheduling with Task Scheduler (Windows) or Cron (Linux/Mac)
If you want to run the script automatically without keeping it open:

**Windows Task Scheduler:**
1. Open Task Scheduler and create a new task.
2. Set the trigger to run daily at 8:00 AM.
3. Set the action to run `jupyter notebook` and provide the script path (`Project.ipynb`).

**Linux/Mac (Cron Job):**
1. Open the terminal and type `crontab -e`
2. Add the following line to schedule it at 8:00 AM daily:
   ```sh
   0 8 * * * /usr/bin/jupyter notebook /path/to/Project.ipynb
   ```
3. Save and exit.

## Troubleshooting
- If the script fails to run, ensure that all dependencies are installed.
- Check your internet connection if the scraper fails to fetch data.
- If the website structure changes, update the parsing logic accordingly.

## License
This project is open-source and free to use.

## Author
Jubin Thomas

Happy Scraping! 🚀

