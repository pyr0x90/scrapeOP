# scrapeOP
A python package for scraping oddsportal.com

Oddportal.com [1] is a tremendous website containing both historical and future betting odds concerning a wide range of sports and bookamers. With the emergence of sports analytics and machine learning, it has become possible for anyone to create data-based betting strategies, taking into considerations both market-related figures (odds values, variations, differentials between bookmakers) and sport-related metrics of performance of any team. In order to perform this task, the very minimal data required is the historical results and betting odds (closing odds are usually preferred) which you can then use to create Machine Learning and Deep Learning models to infer probabilities of victories, and to analyze wheteher or not any given team is being undervalued or overvalued by any fiven bookmaker. The oddsportal website is one of the largest publicly open odds database, however its format and architecture are not very pleasing to deal with, therefore one need a bit of time to build tools to collect the data on their website. This package offers a comprehensive interface (sort of unofficial API) to collect odds and save the data into a comprehensive csv format. <br />

Functionalities : 
- Multiple sports supported : soccer, basketball, esports, darts, tennis, baseball, rugby, american football [list to be expanded soon!]
- Mutiple functionalities : collect historical odds, current season only, upcoming games, specific season only
- Collects all available bookmakers odds for each game
- Collects the final result
- Automatically sort the data by date <br />

The main functions which you can use are the following one : 
1. scrape_oddsportal_historical(sport = 'soccer', country = 'france', league = 'ligue-1', start = '2010-2011', nseason = 5, current_season = 'yes')
2. scrape_oddsportal_current_season(sport = 'soccer', country = 'finland', league = 'veikkausliiga', season = '2020')
3. scrape_oddsportal_specific_season(sport = 'soccer', country = 'finland', league = 'veikkausliiga', season = '2019', max_page = 2)
4. scrape_oddsportal_next_games(sport = 'soccer', country = 'finland', league = 'veikkausliiga', season = '2019') <br />

You can also have a look at the functions.py source code in order to understand the mechanics and eventually adapt the code to your own purpose. In the functions.py script, I distinguished 3 types of sports, according to the sport-related format of outcome (either 1X2, 12, and various types of score : tennis-alike, football-alike, baseball-alike). <br />

[1] https://www.oddsportal.com/ <br />

NB : This package is purposed for educational use only, not for any commmercial purpose in any way. I am not related to any mean with the oddsportal website. 
