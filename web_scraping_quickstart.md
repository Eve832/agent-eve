# Web scraping quickstart with BeautifulSoup

This guide helps you create a Python script that scrapes a website using BeautifulSoup. You'll install the required packages, write a basic scraper, and run it to extract data from a webpage.

## What you'll achieve

After following this guide, you'll have:
- BeautifulSoup and requests installed in your Python environment
- A working Python script that fetches and parses HTML
- The ability to extract specific elements from a webpage

## Before you begin

- Python 3.7 or later installed on your system
- A terminal or command prompt
- An internet connection

## Install required packages

Install BeautifulSoup and the requests library using pip.

```bash
pip install beautifulsoup4 requests
```

Verify the installation:

```bash
python -c "import bs4; import requests; print('Installation successful')"
```

You should see `Installation successful` in your terminal.

## Create your first scraper

Create a new file named `scraper.py` and add the following code:

```python
import requests
from bs4 import BeautifulSoup

# Fetch the webpage
url = "https://example.com"
response = requests.get(url)

# Check if the request was successful
if response.status_code == 200:
    # Parse the HTML content
    soup = BeautifulSoup(response.text, 'html.parser')
    
    # Extract the page title
    title = soup.find('title')
    if title:
        print(f"Page title: {title.text}")
    
    # Extract all paragraph text
    paragraphs = soup.find_all('p')
    for p in paragraphs:
        print(p.text.strip())
else:
    print(f"Failed to fetch page. Status code: {response.status_code}")
```

## Run the script

Execute the script from your terminal:

```bash
python scraper.py
```

The script prints the page title and all paragraph text from the example.com webpage.

## Extract specific elements

Modify the script to target specific HTML elements. Use CSS selectors or BeautifulSoup methods:

```python
import requests
from bs4 import BeautifulSoup

url = "https://example.com"
response = requests.get(url)

if response.status_code == 200:
    soup = BeautifulSoup(response.text, 'html.parser')
    
    # Find elements by class
    elements = soup.find_all(class_='your-class-name')
    
    # Find elements by ID
    element = soup.find(id='your-id')
    
    # Use CSS selectors
    links = soup.select('a[href]')
    for link in links:
        print(link.get('href'))
```

## Next steps

- Review the [BeautifulSoup documentation](https://www.crummy.com/software/BeautifulSoup/bs4/doc/) for advanced parsing techniques
- Learn about handling different HTML structures and nested elements
- Explore error handling for network requests and missing elements
