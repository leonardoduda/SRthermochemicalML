<h1>Advancements in Thermochemical Biomass Conversion: A Systematic Review of AI and ML Techniques (2014-2024)</h1>
<h2>Repository Description</h2>

This repository contains the Python scripts used in the paper "Advancements in Thermochemical Biomass Conversion: A Systematic Review of AI and ML Techniques (2014-2024)". Each script is designed to perform specific data extraction, analysis, and visualization tasks related to the systematic review of AI and ML techniques in thermochemical biomass conversion. The scripts were primarily executed on Google Colab.
1. Extraction of Author Information and Countries from DOIs using BeautifulSoup and Requests (SpringerLink)

Filename: extract_author_info_springerlink.py

Description:
This script extracts the first author's information and their country of origin from DOIs. It utilizes the CrossRef API to fetch author data and BeautifulSoup to parse the HTML content from the DOI's webpage to extract affiliation information.

Key Libraries:

    requests
    BeautifulSoup
    re

Usage:

    List DOIs in the dois list.
    Fetch and parse data using CrossRef and BeautifulSoup.
    Print the extracted country for each DOI.

Requirements:

    Install requests and beautifulsoup4.

python

import requests
from bs4 import BeautifulSoup
import re
...

2. Extraction of Author Information and Countries from DOIs using Selenium and Firefox Gecko (ScienceDirect)

Filename: extract_author_info_sciencedirect.py

Description:
This script extracts author information and country data from DOIs using Selenium to interact with the webpage and extract dynamic content. It uses the CrossRef API to get the first author's name and then scrapes the DOI's webpage for affiliation data.

Key Libraries:

      requests
      selenium
      csv

Usage:
List DOIs in the dois list.
Set up Selenium with Firefox GeckoDriver.
Fetch and parse data using Selenium.

Requirements:

 Install requests, selenium, and firefox-geckodriver.

    python
    
    import requests
    from selenium import webdriver
    from selenium.webdriver.firefox.service import Service
    from selenium.webdriver.common.by import By
    from selenium.webdriver.support.ui import WebDriverWait
    from selenium.webdriver.support import expected_conditions as EC
    import time
    import csv
    ...

3. Extraction of Metadata from Academic Publications - Analysis of DOI, Country of Origin, Year of Publication, and Citation Count

Filename: extract_metadata_academic_publications.py

Description:
This script extracts metadata such as the year of publication and citation count from a list of DOIs using the CrossRef API. It loads a CSV file containing DOIs and countries, retrieves the required metadata, and saves the results in a new CSV file.

Key Libraries:

    pandas
    requests
    google.colab.files

Usage:

    Upload the CSV file containing DOIs and countries.
    Retrieve year of publication and citation count for each DOI using CrossRef.
    Save the results to a new CSV file.

Requirements:

    Install pandas and requests.

python

    import pandas as pd
    import requests
    ...

4. Analysis of Publications and Citations by Country and Year

Filename: analysis_publications_citations.py

Description:
This script analyzes the number of publications and citations by country and year. It reads a CSV file containing publication data, maps country names to their abbreviations, and visualizes the data using Matplotlib.

Key Libraries:

    pandas
    matplotlib

Usage:

    Load the CSV file containing publication data.
    Map country names to abbreviations and create a pivot table.
    Plot the number of publications and total citations per year.

Requirements:

    Install pandas and matplotlib.

python

    import pandas as pd
    import matplotlib.pyplot as plt
    ...

5. Classification and Separation of References by Source of DOI

Filename: classify_separate_references.py

Description:
This script classifies and separates references by the source of their DOIs. It categorizes DOIs into various sources (e.g., Scopus, Web of Science, SpringerLink, ScienceDirect, PubMed) and saves the categorized references into separate CSV files.

Key Libraries:

    pandas
    google.colab.files

Usage:

    Upload the CSV file containing DOIs.
    Categorize DOIs and save the results to separate CSV files for each source.

Requirements:

    Install pandas.

python

    import pandas as pd
    from google.colab import files
    ...

How to Run the Scripts

Clone the Repository:

      git clone <repository_url>
      cd <repository_directory>

Install Required Libraries:

    pip install -r requirements.txt

Execute the Scripts:

Each script can be run in a Google Colab environment. Upload the necessary CSV files as specified in the script descriptions and follow the instructions provided in the script headers.

Feel free to customize the descriptions and usage instructions according to the specific details of each script.
