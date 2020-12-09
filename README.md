# WSBScraper

Search top r/wallstreetbets posts for specified tickers (or really any keyword) to keep up with the discussion!

## Usage
```
./wsbscpr.py [-h] -n NUMPOSTS -t TICKERS [TICKERS ...]

-n NUMPOSTS Number of hot posts to search
-t TICKERS  List of tickers to search comments for
-h HELP     Help message
```
For example:
```
./wsbscrper -n 10 -t PLTR TSLA GOOG
```

## Installation
WSBScraper uses [PRAW](https://praw.readthedocs.io/en/latest/ "PRAW") internally, and thus requires authorization through your reddit account. You can do so easily by following the first section of [this post](https://towardsdatascience.com/scraping-reddit-data-1c0af3040768 "this").

```
git clone ...
pip3 install -r requirements.txt
echo 'SECRET=your_secret_here' >> .env
echo 'ID=your_client_id_here' >> .env
echo 'USER_AGENT=your_user_agent_here' >> .env
```

You may need to set the correct path to your desired python3 interpreter in the shebang of [wsbscrper.py](wsbscrper.py) (or just run via ```python3 wsbscrper.py ...```).
