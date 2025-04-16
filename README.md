# VacancyMail Web Scraper
======================

A Python script that automatically scrapes job listings from VacancyMail Zimbabwe and saves them to a CSV file.

## Table of Contents
---------------

* [Features](#features)
* [Requirements](#requirements)
* [Installation](#installation)
* [Usage](#usage)
* [How It Works](#how-it-works)
* [Schedule](#schedule)
* [Error Handling](#error-handling)
* [CSV Structure](#csv-structure)

## Features
--------

* Automatically scrapes job listings from VacancyMail Zimbabwe
* Saves data to a structured CSV file
* Scheduled daily execution at 09:15
* Error handling with detailed logging
* Emoji-enhanced console output for better visibility

## Requirements
------------

* Python 3.6+
* Required packages:
  * `requests`
  * `beautifulsoup4`
  * `schedule`
  * `csv` (built-in)

## Installation
------------

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/vacancymail-scraper.git
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
-----

1. Run the script:
   ```bash
   python web_scraper.py
   ```
2. The script will:
   * Run immediately for testing
   * Set up daily scheduled execution
   * Save data to `scraped_jobs.csv`

## How It Works
--------------

The script performs the following operations:

1. Sends a GET request to VacancyMail's jobs page
2. Parses HTML content using BeautifulSoup
3. Extracts job details:
   * Job title
   * Company name
   * Location
   * Expiry date
   * Job description
4. Writes data to a CSV file

## Schedule
---------

The script is configured to:
* Run immediately on startup (for testing)
* Execute daily at 09:15
* Continue running until manually stopped (Ctrl+C)

## Error Handling
--------------

The script includes comprehensive error handling for:
* Failed HTTP requests
* Invalid HTML structure
* CSV writing errors
* Missing job listing elements

## CSV Structure
-------------

The output CSV file contains the following columns:
| Column Name | Description |
|-------------|-------------|
| Job Title   | Job position title |
| Company     | Hiring company name |
| Location    | Job location |
| Expiry Date | Job posting expiry date |
| Job Description | Detailed job description |

## Notes
-----

* The script uses emoji indicators for better console visibility:
  * ⏰: Start time
  * 📡: HTTP request
  * ✅: Success
  * ❌: Error
  * 🎉: Completion
  * 📅: Schedule
  * 🕒: Running
* The script will continue running until manually stopped with Ctrl+C
