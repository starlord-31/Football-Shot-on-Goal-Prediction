# Football-Shot-on-Goal-Prediction

The datset has been scraped from understat.com which contains data related to shots on goal in football's top 5 leagues and the russian league from 2014-15 season.

Problem Description: Predicting Football Shots on Goal Outcome

This project aims to develop a machine-learning model to predict the outcome of football shots on goal. Utilizing a dataset comprising information on player positions, game situations, and shot characteristics, the objective is to analyze, preprocess, and model the data. The primary focus is on experimenting with various machine learning algorithms to determine the most effective one for predicting shot outcomes. The end goal is to provide a valuable tool for coaches, analysts, and players, enabling them to assess shot probabilities and optimize strategic decision-making during matches.

## Running locally with gunicorn/waitress
1. Clone this repository on your computer.
3. Install dependencies from ```Pipfile``` by running command:
```Python
pipenv install
```
3. Activate virtual environment:
```Python
pipenv shell
```
4. Run service with gunicorn:
```Python
pipenv run gunicorn --bind 0.0.0.0:9696 predict:app
```
Or with waitress:
```Python
waitress-serve --listen=0.0.0.0:9696 predict:app
```
5. Run [predict_test.py]() in a different terminal to see the predicted player value of a given player_attributes.
