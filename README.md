
![alt text](https://github.com/ibrahimceyisakar/Content-Sentiment-Analysis/blob/main/SentimentAnalysis-1.png?raw=true)

<!-- /code_chunk_output -->


## Content-Sentiment-Analysis
<!-- code_chunk_output -->

- [Content-Sentiment-Analysis](#content-sentiment-analysis)
  - [Description](#description)
  - [Installation](#installation)
  - [Classes](#classes)
  - [Note](#note)
  - [Used Packages/Modules](#used-packagesmodules)
### Description

This project is a collection of python classes that can be used to scrape comments from Instagram and Youtube, translate them to English, and perform sentiment analysis on them. The results can then be exported to a CSV file.
    
### Installation
  1. Clone the repository.
  2. Open a terminal in the project folder.
  3. Create a virtual environment in the project folder.
  4. Activate the virtual environment.
  5. Install the required packages using the requirements.txt file.
  6. Create a ```settings.py``` file in the project folder (example below).
  7. Use the classes in the project folder.


For example:
```
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
touch settings.py
python youtube-analysis.py
```

```
# settings.py

# no credentials needed scraping youtube comments 
INSTAGRAM_USERNAME = "YOUR_USERNAME"
INSTAGRAM_PASSWORD = "YOUR_PASSWORD"
INSTAGRAM_CONTENT_URL = "POST_URL"
YOUTUBE_CONTENT_URL = "VIDEO_URL"
```

### Classes
    BaseCommentScraper          (abstract class for child scraper classes)      
    InstagramCommentScraper     (login credentials required)
    YoutubeCommentScraper       (no credentials required)
    TextTranslator              (no credentials required)    
    SentimentAnalysis           (no credentials required)
    CSVExporter                 (no credentials required)
    
### Note
The InstagramCommentScraper class requires login credentials to work. You can create a new Instagram account and use it to scrape comments. The account will be banned if you use it to scrape too many comments in a short period of time. You can also use your own account, but it is not recommended. The YoutubeCommentScraper class does not require login credentials.


### Used Packages/Modules
    https://github.com/adw0rd/instagrapi                    for InstagramCommentScraper 
    https://github.com/alexmercerind/youtube-search-python  for YoutubeCommentScraper   
    https://github.com/nidhaloff/deep-translator            for TextTranslator              
    https://github.com/sloria/TextBlob                      for SentimentAnalysis       
    https://github.com/fnielsen/afinn                       for SentimentAnalysis       


mkkm
