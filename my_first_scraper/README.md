# Welcome to My First Scraper
GitHub Trending Scraper
This script allows you to scrape the trending repositories on GitHub.
It retrieves information such as the developer, repository name, and number of stars for each
trending repository.
Prerequisites
To run this script, you need to have the following installed:
Python (version 3.6 or higher)
requests library
beautifulsoup4 library
You can install the required libraries using pip:
pip install requests beautifulsoup4

## Task
What is the problem? And where is the challenge?
The problem and challenge in the provided code lie in the implementation of the test cases. 
The code itself seems to be functional and performs the scraping and data transformation tasks correctly.
 However, the test cases included in the code are failing, which is why the overall score is low.
Let's analyze the test cases and the issues they highlight:
TEST EXTRACT:
The expected output is an empty string.
The expected return value is not specified.
The test code attempts to extract data from a trending GitHub page using the request_github_trending and extract functions.
The assertion self.assertTrue(len(data) > 5) fails, indicating that the extracted data does not have more than 5 elements.
The error message suggests that the object of type 'Response' has no length. This could be due to an issue with the data extraction or the handling of the response object.
TEST FORMAT:
The expected output is an empty string.
The expected return value is not specified.
The test code attempts to format the data extracted from the GitHub page using the request_github_trending, extract, transform, and format functions.
The assertion self.assertTrue(isinstance(output_str, str)) fails, indicating that the formatted output is not a string.
The error message suggests that False is not true. This could be due to an issue with the formatting logic or the data types being used.
TEST REQUEST GITHUB TRENDING:
The expected output is an empty string.
The expected return value is not specified.
The test code calls the request_github_trending function and asserts that the returned page object is an instance of requests.Response.
The assertion self.assertTrue(isinstance(page, requests.Response)) passes, indicating that the response object is of the correct type.
TEST TRANSFORM:
The expected output is an empty string.
The expected return value is not specified.
The test code attempts to transform the extracted data using the request_github_trending, extract, transform functions.
The assertion self.assertTrue(len(array_of_dict) > 5) fails, indicating that the transformed data does not have more than 5 elements.
The assertion self.assertTrue(len(array_of_dict) == len(data)) fails, suggesting that the number of transformed elements is not equal to the number of extracted elements.
The error message suggests that the object of type 'Response' has no length. This could be due to an issue with the data transformation or the handling of the response object.
In summary, the challenge lies in properly implementing the test cases to ensure that the extracted data is correct, the formatting logic produces the expected output, and the response
 object is handled correctly throughout the code. Analyzing and addressing the issues in the test cases should help improve the overall score and ensure the functionality of the scraper.

## Description
How have you solved the problem?
Import the necessary libraries:
requests library is used to send HTTP requests and retrieve the HTML content of a web page.
BeautifulSoup from the bs4 library is used for parsing and extracting data from HTML.
Define the request_github_trending function:
This function takes a URL as input and sends a GET request to that URL using the requests.get() function.
It includes a User-Agent header to mimic a web browser and avoid being blocked by the server.
The function returns the response object.
Define the extract function:
This function takes a page object as input, which can be either a requests.Response object or raw HTML content.
If the input is a requests.Response object, it retrieves the HTML content from the content attribute.
It uses BeautifulSoup to parse the HTML content and finds all the <article> elements with the class Box-row.
The function returns a list of HTML elements representing the repositories.
Define the transform function:
This function takes a list of HTML elements representing repositories as input.
It iterates over each repository element and extracts the developer, repository name, and number of stars.
The extracted information is stored as a dictionary and appended to a list.
The function returns a list of dictionaries, where each dictionary represents a repository.
Define the format function:
This function takes a list of dictionaries representing repositories as input.
It iterates over each repository dictionary and formats the developer, repository name, and number of stars into a string.
The formatted strings for each repository are concatenated and returned as a single string.
The main part of the code:
The URL for GitHub's trending page is defined.
The request_github_trending function is called to retrieve the page content.
The extract function is called to extract the relevant HTML elements representing repositories.
The transform function is called to transform the HTML elements into a list of dictionaries.
The format function is called to format the list of dictionaries into a string.
The resulting string is printed, which contains the developer, repository name, and number of stars for each trending repository.
This code can be customized by modifying the URL or adding additional data extraction and formatting logic as per the requirements.

## Installation
How to install your project? npm install? make? make re?
To run this script, you need to have the following installed:
Python (version 3.6 or higher)
requests library
beautifulsoup4 library
pip install requests beautifulsoup4

## Usage
How does it work?
Import the necessary libraries:
import requests
from bs4 import BeautifulSoup
import csv
```
./my_project argument1 argument2
```

### The Core Team


<span><i>Made at <a href='https://qwasar.io'>Qwasar SV -- Software Engineering School</a></i></span>
<span><img alt='Qwasar SV -- Software Engineering School's Logo' src='https://storage.googleapis.com/qwasar-public/qwasar-logo_50x50.png' width='20px'></span>
