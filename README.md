Books to Scrape Category Scraper

OVERVIEW
========

This application scrapes book information from the Books to Scrape website and exports the results to a CSV file.

The script:

- Connects to https://books.toscrape.com/
- Selects a specific category (e.g., Mystery)
- Processes all books in the category
- Extracts product information including:
  * UPC
  * Product Type
  * Price (excluding tax)
  * Price (including tax)
  * Tax
  * Availability
  * Number of Reviews
- Writes the results to a CSV file


PREREQUISITES
=============

- Python 3.9 or later
- Internet connection


CREATE A VIRTUAL ENVIRONMENT
============================

Open a command prompt or terminal and navigate to the project folder.

Windows:

    python -m venv venv

Linux/macOS:

    python3 -m venv venv


ACTIVATE THE VIRTUAL ENVIRONMENT
================================

Windows Command Prompt:

    venv\Scripts\activate

Windows PowerShell:

    .\venv\Scripts\Activate.ps1

Linux/macOS:

    source venv/bin/activate

When activation is successful, your prompt should display:

    (venv)


INSTALL REQUIRED PACKAGES
=========================

Install dependencies using pip:

    pip install requests beautifulsoup4

Optionally create a requirements file:

    pip freeze > requirements.txt

To install from a requirements file:

    pip install -r requirements.txt


PROJECT STRUCTURE
=================

project_folder/

    scraper.py
    category.csv
    requirements.txt
    README.txt


RUNNING THE APPLICATION
=======================

Execute the scraper:

    python scraper.py

or

    python3 scraper.py


OUTPUT
======

The application generates:

    category.csv

The CSV file contains the following columns:

- UPC
- Product Type
- Price (excl. tax)
- Price (incl. tax)
- Tax
- Availability
- Number of Reviews


CHANGING THE CATEGORY
=====================

To scrape a different category, modify the following line in the script:

    if cat == "Mystery":

Examples:

    if cat == "Science Fiction":

    if cat == "Travel":

    if cat == "Historical Fiction":


DEACTIVATE THE VIRTUAL ENVIRONMENT
==================================

When you are finished:

    deactivate
