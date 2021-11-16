# Betting the NFL Over/Under - A Data Science Perspective #

**In the United States, over 40 million people bet on National Football League (NFL) games each year, wagering over $12 billion dollars annually. One of the most popular wagers offered by sportsbooks is the Over/Under (O/U) bet, in which the bettor chooses whether the Total Score of the contest will be over or under the posted O/U value. In this study, team statistics as well as game conditions are considered in a regression model to determine whether the O/U bet can be predicted with sufficient accuracy as to make the O/U bet profitable. The complete study can be viewed at the following links:**
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
**In comparing the Total Score with the O/U values posted by the sportsbooks, both are found to exhibit a normal distribution but with Total Score revealing a much larger range. Large errors between Total Score and O/U reside mainly to the upside. One of the main findings of this analysis is that the Over has a significantly higher winning percentage in the first ten weeks of the season than in the last seven weeks.**

![](https://github.com/titansat74/NFL_Over_Under/blob/main/README_files/fig7.png)

**The decline in Total Points later in the season, which corresponds to the reduction in Over winning percentage, seems to be directly related to the decline in passing yardage, which accompanies a decrease in temperature as the season progresses.**

**Notebook for exploratory data analysis:**
> * [EDA Notebook](https://github.com/titansat74/NFL_Over_Under/blob/main/notebooks/nfl_eda.ipynb)

## 4. Modeling ##
**The feature set was trained on four regression models (Ordinary Least Squares, Ridge, Random Forest, and XGBoost) with recursive feature elimination and hyperparameter tuning used to optimize the models. A description of the metrics used in the analysis can be found [here](https://github.com/titansat74/NFL_Over_Under/blob/main/docs/NFL_Over_Under%20Metrics.pdf). Random Forest yielded the best results with 37 features. No one feature was dominant in any of the models; however, features involving offensive passing, particularly that of the visiting team, were consistently among the most important features.**
![](https://github.com/titansat74/NFL_Over_Under/blob/main/README_files/Table2.png)

**To further optimize the Random Forest results, threshold tuning was performed to determine which subset of games should be wagered to maximize betting efficiency. A threshold of -1 for the Under and +2 Over was found to be most optimal.**
![](https://github.com/titansat74/NFL_Over_Under/blob/main/README_files/fig20.png)

**Notebook for modeling analysis:**
> * [Modeling Notebook](https://github.com/titansat74/NFL_Over_Under/blob/main/notebooks/nfl_modeling.ipynb)

## 5. Summary ##
**The major finding of this study are as follows:**
> * **There is no one dominant feature guiding the prediction of total score, but passing yards is consistently the most important single statistic**
> * **Passing yardage is significantly affected by temperature, which is not adequately considered in the determination of the Over/Under**
> * **Wind is also a significant factor in total score output**
> * **The most important defensive feature is visiting defense red-zone percentage**
> * **The Random Forest model with 37 features is the most optimal model, yielding a seasonal return of 42% for the test set upon application of threshold tuning**
## 6. Future Work ##
**This study can be improved in the future with the following considerations:**
> * **More recent data are available for implementation into the model**
> * **Evolution of features over time can be considered in a time series treatment of the problem**
> * **Varying the bet size through threshold tuning can provide further model optimization**
