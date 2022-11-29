
## Introduction
This project creates and updates the table of biorxiv and medrxiv pre-prints that I have on my [website](https://tjburns08.github.io/biorxiv_medrxiv_history.html). This project can be generalized to any tweets from any user.

This project solves the following problems:
1. How to stay ahead of the pre-print literature in your field and in general.
2. How to determine which pre-prints are worth paying attention to. 

## How to use
After you pip install the requirements.txt file:
1. Go to src/
2. Run scrape_tweets.py. Note that the file users.csv contains the twitter users you want to scrape. In this case, it's biorxiv and medrxiv. This will produce output as csv files that sit in data/.
3. Run biorxiv_medrxiv_history.ipynb to get the updated table. 
4. To get the html file, run jupyter nbconvert --to html --no-input biorxiv_medrxiv_history.ipynb

## Why it works
Biorxiv and medrxiv preprint servers create a tweet every time a new manuscript is uploaded. The tweet contains the title of the paper as well as a link to the paper. Scraping the tweet archives of the corresponding twitter usernames gives you the corpus of everything that has ever been uploaded to the servers along with the tweet metadata. As such, you can see what was uploaded when, and what kind of reception it got on twitter. This is useful in determining what papers are going to be "seminal" down the line. One would otherwise have to wait a year or more for the pre-print to make it through peer review (if it does) and then wait for it to accumulate citations. 

## Possible extensions
Any twitter username, bot or otherwise, that exclusively uploades papers, is fair game for this tool. Cell, Science, and Nature do not do this. Other users like Single Cell Papers (@scell_papers) do. 

In a more general sense, you can take this approach for news articles. You can either harvest users like AP or Bloomberg, or you can harvest the tweets of independent journalists. 

## Acknowledgements
The [snscrape project](https://github.com/JustAnotherArchivist/snscrape), for their amazing work that makes this type of data curation possible. If anything, I hope this project brigs awareness to their work. I also hope that my project contibutes to theirs by providing an example of how to use their python package, which has not been documented yet as their command line interface has. 