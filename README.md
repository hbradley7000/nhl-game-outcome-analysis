# NHL Game Outcome Analysis

## Project Overview
This project explores how NHL team performance statistics can be used to classify game outcomes and identify which in-game metrics are most associated with winning.

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

The data comes from the [NHL Game Data dataset on Kaggle](https://www.kaggle.com/datasets/martinellis/nhl-game-data/data).

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
- Power-play opportunities
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

The models were evaluated across several feature sets using accuracy and confusion matrices.

| Feature Set | Decision Tree Accuracy | Random Forest Accuracy |
|---|---:|---:|
| 8 features | 76.36% | 78.50% |
| 7 features | 76.34% | **79.09%** |
| 4 features | 74.66% | 75.41% |
| 3 features | **74.12%** | 73.89% |

The strongest model was the **Random Forest classifier using seven features**, which achieved **79.09% accuracy**.

The seven features were:

- Shots
- Hits
- Penalty minutes
- Faceoff win percentage
- Giveaways
- Takeaways
- Blocked shots

Removing power-play opportunities slightly improved Random Forest performance from **78.50% to 79.09%**, suggesting that this variable added limited predictive value within this feature set.

### Best Model Confusion Matrix

The best-performing Random Forest model produced:

- 3,116 correctly classified losses
- 3,124 correctly classified wins
- 791 losses incorrectly classified as wins
- 859 wins incorrectly classified as losses

This shows relatively balanced classification performance across wins and losses.

## Feature Importance

For the full Random Forest model, the most influential features were:

| Feature | Importance |
|---|---:|
| Faceoff Win Percentage | 18.00% |
| Shots | 14.07% |
| Hits | 13.60% |
| Blocked Shots | 12.81% |
| Giveaways | 12.80% |
| Penalty Minutes | 11.12% |
| Takeaways | 9.87% |
| Power-Play Opportunities | 7.73% |

**Faceoff win percentage** was the most influential feature in both the Random Forest and Decision Tree models, while power-play opportunities had the lowest importance among the eight variables analyzed.

## Key Takeaways

- Random Forest generally outperformed the Decision Tree across the tested feature sets.
- The strongest model achieved **79.09% accuracy** using seven team-performance statistics.
- Removing power-play opportunities slightly improved model accuracy, suggesting that additional features do not always improve classification performance.
- Faceoff win percentage was the most influential variable in both models.
- Model performance declined as the feature set was reduced further, showing that several game statistics contributed useful information.
- The project demonstrates how feature selection can affect both model performance and interpretability.

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
