# hws

**hws** allows you to extract any information from any webpage using humans. To use provide your wao.ai API key, a set of urls, 
and a description for what they want scraped. Then, that job gets sent to our workers.
Depending on the number of URLs, the amount of time spent on a request can vary from 10 minutes to 12 hours. 
When the URLs are all resolved the results from the different jobs will be stored in the given .txt or .csv file.

## Design Goals 

1. Users should be able to use the CLI to easily get results from the WorkAround platform
2. Simple commands 
3. Runs quickly and smoothly 
  

## Features

* Upload any number of urls and extract any information from the page
* Extract using human-readable descriptions of the content
* Extract as many fields per page as needed

## Basic Usage 

```
$ workaroundaround-job-scraper login
# API Key (Get from your wao.ai dashboard): ********
# Saved to ~/.wao-scraper/api_key.txt

# Successfully Logged in! 
OR 
# Key not recognized... 
$ workaround-job-scraper scrape urls.txt 

# Our workers have strated scraping for you! Run workaround-job-scraper status to see job status and download to a file   

$ workaround-job-scraper status 

# <NUMBER>% of URLs scraped! Results written to an output file
```

The content of the urls.txt

```
https://example.com/url/path.txt
https://example.com/url/path.txt
https://example.com/url/path.txt
```

For multiple fields use a `fields.txt` file.

```
$ workaround-job-scraper scrape -f fields.txt urls.txt
```

Some examples of `fields.txt`...

```
What is the email address on the page?
What is the phone number on the page?
```

```
What is the price of the studio aparmtnet?
What is the price of the 1BR aparmtnet?
What is the price of the 2BR aparmtnet?
```

## Commands

| Command                         | Description                         |
| ------------------------------- | ----------------------------------- |
| `login [apikey]`                | Allows user to input wao.ai API Key |
| `scrape -d <description> urls.txt`         | Begins scraping by uploading urls and using the description as the extraction.   |
| `scrape -f fields.txt urls.txt`         | Begins the scraping of a URL file   |
| `status`                        | Outputs number of URLs scraped      |

## Flags

| Flag     | Description                                                                               |
| -------- | ----------------------------------------------------------------------------------------- |
| `-n`     | If put on job, your WorkAround email will receive a notification when the job is complete |
