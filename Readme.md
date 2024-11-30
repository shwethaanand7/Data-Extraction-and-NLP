## Task Assigned by <a href='https://blackcoffer.com'>Black Coffer</a>

## Data Extraction and NLP

This project aims to extract textual data articles from given URLs and perform text analysis to compute variables. The code is written in Jupyter Notebook for its flexibility compared to scripting.

## Prerequisites

Before running the code, make sure to install the required packages by running the following command:

```bash
python3 install -r requirements.txt
```

## Approach

The project follows the following steps:

- input data: Read input data from input.xlsx using pandas.
- Web Scraping: Use the requests module to get the raw HTML content from the URLs specified in the input file.
  Utilize the BeautifulSoup module to perform web scraping.
- Find the title of the article using the `<h1>` tag and obtain the content using the `<div>` tag and class name selectors.
- Since different articles may have different class selectors, try-except blocks are used to handle any exceptions.
- Text Analysis: Perform text analysis using the NLTK library.
- Use the Punkt tokenizer to divide the text into sentences using the sent_tokenize function.
- Remove stop words (common words like 'the', 'and', 'I', etc.) using the NLTK stopwords module.
- Tokenize the text into words using the word_tokenize function.
- Estimate the number of syllables using a simple syllable estimator.
- Compute Variables: Compute the required variables by looping through multiple URLs and performing various calculations.
- Store Results: Store the variables in lists and insert them into a dictionary with the specified column names.
- Export Results: Export the results to Output Data Structure.xlsx.

## Output

The output file Output Data Structure.xlsx will contain the computed variables for each article.

Note: During the analysis, a few web pages were not found and couldn't be scraped.
Please refer to the code file in the Jupyter Notebook format for a detailed implementation.
