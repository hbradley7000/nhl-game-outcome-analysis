# NHL Game Outcome Analysis

## Project Overview
This project explores whether NHL team performance statistics can be used to classify game outcomes and identify which in-game metrics are most associated with winning.

Using historical NHL game data, I combined multiple datasets, cleaned and prepared the data, trained machine learning classification models, and compared their performance across different feature sets.

## Objective
The goal of the project was to:

- Combine NHL game and team-level datasets into a usable analytical dataset
- Clean and validate the data for machine learning
- Compare Decision Tree and Random Forest classifiers
- Test how different combinations of team statistics affect model performance
- Identify which features are most influential in classifying wins and losses
- Visualize and interpret model results

## Dataset
The data comes from the **NHL Game Data** dataset available on Kaggle.

The project combines information from:

- Game-level data
- Team game statistics
- Team information

The dataset is downloaded programmatically using `kagglehub`.

## Tools & Technologies

- Python
- pandas
- NumPy
- scikit-learn
- matplotlib
- Kaggle / kagglehub
- Jupyter Notebook / Google Colab

## Machine Learning Models

Two classification models were evaluated:

### Decision Tree
A Decision Tree classifier was trained to establish a baseline and examine how individual variables contribute to game outcome classification.

### Random Forest
A Random Forest classifier was used to compare performance against the Decision Tree and evaluate feature importance across multiple predictors.

## Features Analyzed

The project evaluates NHL team statistics including:

- Shots
- Hits
- Penalty minutes
- Faceoff win percentage
- Giveaways
- Takeaways
- Blocked shots

Multiple feature subsets were tested to examine how model performance changed as variables were removed.

## Model Evaluation

Models were evaluated using:

- Accuracy
- Confusion matrices
- Actual vs. predicted outcomes
- Feature importance

The project also compares Decision Tree and Random Forest results across different feature combinations.

## Results

The Decision Tree and Random Forest models were compared across multiple feature sets using accuracy and confusion matrices.

The Random Forest model generally provided stronger classification performance and was also used to evaluate feature importance across NHL team statistics.

Specific model accuracy results and feature importance findings are available in the notebook.

## Key Takeaways

This project demonstrates an end-to-end machine learning workflow including:

1. Downloading data from an external source
2. Combining multiple datasets
3. Cleaning and validating records
4. Selecting and engineering model features
5. Splitting data into training and testing sets
6. Training classification models
7. Evaluating model performance
8. Comparing feature importance
9. Visualizing analytical results

## Future Improvements

A future version of the project could create a true pre-game prediction model by calculating rolling team statistics from previous games rather than using statistics recorded during the game.

Additional improvements could include:

- Chronological train/test splitting
- Cross-validation
- Hyperparameter tuning
- Additional classification models
- ROC-AUC and precision/recall analysis
- Rolling team performance metrics
- Opponent-adjusted statistics

## Repository Contents

`nhl_game_outcome_analysis.ipynb` — Full data preparation, modeling, evaluation, and visualization workflow.

## Author

**Hayden Bradley**  
M.S. Business Analytics  
Saint Mary's College of California
