# Betting the NFL Over/Under - A Data Science Perspective #

**In the United States, over 40 million people bet on National Football League (NFL) games each year, wagering over $12 billion dollars annually. One of the most popular wagers offered by sportsbooks is the Over/Under (O/U) bet, in which the bettor chooses whether the total score of the contest will be over or under to posted O/U value. In this study, team statistics as well as game conditions are considered in a regression model to determine whether the O/U bet can be predicted with sufficient accuracy as to make the O/U bet profitable. The complete study can be viewed at the following links:**
> * [Full Report](https://github.com/titansat74/NFL_Over_Under/blob/main/docs/NFL%20Over_Under%20Analysis.pdf)
> * [Google Sheets Presentation](https://github.com/titansat74/NFL_Over_Under/blob/main/docs/NFL%20Over_Under%20Presentation.pdf)

## 1. Raw Data ##
**Data from 2559 NFL contests were scraped from the [Pro Football Reference](https://www.pro-football-reference.com/) website using the [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/) package. To predict the total score of a contest, game statistics of the teams involved were averaged over their previous five games. These statistics, involving scoring, passing, rushing, special teams, and defense, were combined with data on game conditions to provide a feature space for prediction.
Notebook to acquire data:**
> * [Scraper Notebook](https://github.com/titansat74/NFL_Over_Under/blob/main/notebooks/nfl_scraper.ipynb)

## 2. Data Processing ##
**The raw data were processed into dataframes used for analysis and prediction. A total of 48 features comprise the feature space.
Notebook to generate dataframes:**
> * [Generator Notebook](https://github.com/titansat74/NFL_Over_Under/blob/main/notebooks/nfl_generator.ipynb)

**List of features used in the study:**
> * [Feature List](https://github.com/titansat74/NFL_Over_Under/blob/main/docs/NFL%20Over_Under%20Features.pdf)

## 3. Exploratory Data Analysis ##
**dkfjdlkfj**
![](https://github.com/titansat74/NFL_Over_Under/blob/main/README_files/fig7.png)

## 4. Modeling ##
**Here is a table.**
![](https://github.com/titansat74/NFL_Over_Under/blob/main/README_files/Table2.pdf)

## 5. Summary ##

## 6. Future Work ##

