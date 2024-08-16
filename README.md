# Airlines Reviews Dataset

Welcome to the Airlines Reviews Dataset repository! This project contains a collection of airline reviews from various airlines, providing insights into passenger experiences.

## Overview

The dataset includes reviews for the following airlines:
- British Airways
- Air France
- Emirates
- Qatar Airways
- Qantas Airways
- Singapore Airlines

Each review contains information such as the reviewer’s name, location, date of publication, text content, and various ratings.

## Web Scraping

This dataset was created using web scraping techniques to extract reviews from multiple airline review pages. Web scraping involves programmatically retrieving and parsing data from websites. In this project, Python libraries such as `requests` and `BeautifulSoup` were used to scrape review data from airline review pages.

### How We Scraped the Data

1. **Target Pages**

   We identified the URLs of review pages for each airline. Each page contains a list of reviews with various details.

2. **Sending Requests**

   We sent HTTP GET requests to these URLs to retrieve the HTML content of the pages.

3. **Parsing HTML**

   Using `BeautifulSoup`, we parsed the HTML content to locate and extract relevant data, including:
   - Reviewer's name
   - Location
   - Date of publication
   - Text content of the review
   - Ratings for seat comfort, cabin staff service, food & beverages, inflight entertainment, and value for money
   - Recommendation status

4. **Extracting Data**

   We extracted data by locating specific HTML elements and attributes. For example:
   - **Name**: Extracted from `<span>` tags with `itemprop="name"`.
   - **Date Published**: Extracted from `<time>` tags with `itemprop="datePublished"`.
   - **Ratings**: Extracted from `<span>` tags with the class `star fill`, indicating filled stars.

5. **Combining Data**

   After scraping data from multiple pages for each airline, we combined all the data into a single dataset.

6. **Saving Data**

   The final dataset was saved as a CSV file for ease of use and analysis.

## Dataset

### `airlines_reviews.csv`

This CSV file contains the combined dataset of airline reviews. The columns include:

- `Name`: The name of the reviewer.
- `Location`: The location of the reviewer.
- `Date Published`: The date when the review was published.
- `Text Content`: The body of the review.
- `Seat Type`: The type of seat reviewed.
- `Seat Comfort`: Rating for seat comfort (1-5 stars).
- `Cabin Staff Service`: Rating for cabin staff service (1-5 stars).
- `Food & Beverages`: Rating for food and beverages (1-5 stars).
- `Inflight Entertainment`: Rating for inflight entertainment (1-5 stars).
- `Value For Money`: Rating for value for money (1-5 stars).
- `Recommended`: Whether the reviewer recommends the airline (`yes` or `no`).
