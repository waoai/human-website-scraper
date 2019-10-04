WorkAround Job Scraper CLI Utility

# About

   The Workaround CLI tool allows you to easily use the WorkAround app. You give the CLI their WorkAround API key, a set of urls, 
   and a description for what they want scraped. Then, that job gets sent to our workers.
   Depending on the number of URLs, the amount of time spent on a request can vary from 10 minues to 12 hours. 
   When the URLs are all resolved the results from the different jobs will be stored in the given .txt or .csv file.

# Design Goals 

  1. Non-technical users should be able to use the CLI to easily get results form the WorkAround platform
  2. Simple commands 
  3. Runs quickly and smoothly 
  

# Features
   
# Dependencies

# Usage details 
   '''
   
    $ workaroundaround-job-scraper login <PROVIDE .txt file with API key> 
    
    # Successfully Logged in! 
    OR 
    # Key not recognized... 
    $ workaround-job-scraper scrape urls.txt <provide -n flag for enabling notification when task is complete> 
    
    # Our workers have strated scraping for you! Run workaround-job-scraper status to see job status and download to a file   
    
    $ workaround-job-scraper status 
    
    # <NUMBER>% of URLs scraped! Results written to an output file
  '''
   
