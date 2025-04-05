---
title: "How to Use BeautifulSoup for Web Scraping in Python"
date: 2025-02-25
categories: [Data Mining]
tags: [Python, BeautifulSoup, Web Scraping, Tutorial]
author: Nancy Jiwono
layout: post
description: "Learn how to use BeautifulSoup, a powerful Python library, for web scraping and extracting data from websites."
image: /assets/beautifulSoup/coverBeautifulSoup.png
comments: true
---

## What is Web Scraping?
**Web scraping** is the process of automatically extracting data from web pages. This process is often used when the required data is not available in the form of an API or downloadable file. One of the most commonly used tools for scraping in Python is BeautifulSoup.

## What is BeautifulSoup?
**BeautifulSoup** is a Python library specifically designed to make it easier to extract, parse, and navigate HTML or XML structures. This library is very suitable for scraping because it provides functions that simplify the process of finding specific elements within a web page.

To perform scraping, BeautifulSoup is typically used alongside the requests library, which is used to send a request to a website and retrieve the content of the page (its HTML).

Here a documentation BeautifulSoup, visit the [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/).

## How Does the Scraping Process Work?
The scraping process using BeautifulSoup generally consists of several steps as follows:
1. Sending a Request to the Website
The first step is to send a request to a web page using the **requests** library. From this request, we will get the HTML content of the page. This HTML is what we will process and extract data from.

2. Parsing the HTML with BeautifulSoup
After getting the HTML, we use it as input for BeautifulSoup. BeautifulSoup will read the HTML and structure it into a tree, allowing us to easily navigate and search for specific parts such as `<div>`, `<table>`, `<h1>`, and so on.

3. Finding Relevant HTML Elements
Once the HTML is parsed, we can start looking for specific elements that contain the data we need. For example, if we want to extract data from a table, we will search for the `<table>` tag and its inner elements. BeautifulSoup provides methods such as find() and find_all() to locate elements by their tag or class.

4. Extracting Text or Attributes from Elements
After locating the desired element, we can extract the text content of that element, or attributes like href from an `<a>` tag, or src from an `<img>` tag. We can also clean the data by removing whitespace or any unnecessary characters.

5. Storing or Processing the Data
The extracted data can then be displayed, saved into a CSV or Excel file, or stored in a database depending on the need.

- Inspect view to find `<h3>` tags with the class `country-name`.  
![Find Country Name Inspect Example](/assets/beautifulSoup/inspect.png)  
*Figure 1: Inspecting the HTML structure to locate `<h3>` tags with the class `country-name` for extracting country names using BeautifulSoup.*  

## Study Case
As a real example, we can perform scraping on the following page:

Here a link use to do a study case, visit the [Scrap This Site](https://www.scrapethissite.com/pages/simple/).

On this page, you can find a lot of information about different countries around the world. Each country is displayed in a box that contains:
- The name of the country
- The name of its capital
- The population
- The area size

Using BeautifulSoup, we can:
- Retrieve all elements that represent a country
- Extract the country name from a specific tag
- Extract the capital, population, and area text from other tags within the same element
- Repeat this process for all countries on the page

**Code Example**  
Here are some code examples to find country name, capital, population, and area:

![Find Country Name Example](/assets/beautifulSoup/findh3.png)  
*Figure 1: Code snippet to locate and extract the country name using BeautifulSoup.*  

![Country Name Result Example](/assets/beautifulSoup/h3result.png)  
*Figure 2: The result of extracting country names displayed in the console.*  

![DataFrame Creation Example](/assets/beautifulSoup/dataFrame.png)  
*Figure 3: Code snippet to create a DataFrame from the extracted data for better organization.*  

![DataFrame Result Example](/assets/beautifulSoup/dataFrameResult.png)  
*Figure 4: The resulting DataFrame showing country names, capitals, populations, and areas.*  

![Save to CSV Example](/assets/beautifulSoup/saveCSV.png)  
*Figure 5: The resulting CSV file showing the extracted data, including country names, capitals, populations, and areas.*  

## Why Use BeautifulSoup?
Here are a few reasons why BeautifulSoup is widely used:
- Simple and easy to learn
- Suitable for simple HTML (no need to render JavaScript)
- Provides intuitive methods for element searching (find(), find_all())
- Compatible with other libraries such as requests, pandas, and lxml

## Things to Consider
Before performing scraping, there are a few important things to keep in mind:
- Legality and ethics: Make sure the website you are scraping allows data extraction (check their robots.txt file).
- Don’t overload the server: Avoid sending too many requests in a short period of time.
- Do not misuse the data: Use the scraped data responsibly and avoid violating copyrights.

## Conclusion
Web scraping using BeautifulSoup is a powerful technique for automatically extracting information from websites. By understanding the HTML structure and how to navigate it with BeautifulSoup, you can extract data from nearly any website with statically available content.

--- 
Hope you enjoyed and learned something new! 🎉 

Stay healthy and take care! 💪🏻

Thank youu!!! 