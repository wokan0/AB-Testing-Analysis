# Cookie Cats A/B Testing Analysis

## Introduction

Cookie Cats is a popular mobile puzzle game developed by Tactile Entertainment. The game involves connecting tiles of the same color to progress through levels. The placement of gates, which players encounter as they advance, is crucial for driving in-app purchases and enhancing overall enjoyment. This analysis focuses on evaluating the impact of moving the first gate from level 30 to level 40 on player retention.

### Dataset

The analysis uses the Mobile Games A/B Testing dataset, available [here](https://www.kaggle.com/datasets/yufengsui/mobile-games-ab-testing).

## Notebook Contents

The notebook includes A/B testing on the mobile game dataset using bootstrapping and null-hypothesis tests from the scipy library.

## Data Preprocessing

The dataset, containing around 90,189 records, underwent cleaning and consistency checks. Outliers were identified and removed, resulting in a dataset with variables such as `userid`, `version`, `sum_gamerounds`, `retention_1`, and `retention_7`.

## Exploratory Analysis

Exploratory analysis revealed insights into player behavior, such as the distribution of game rounds played. Users who played less than 30 rounds and the top 1% of players were excluded from the retention analysis.

## A/B Testing

A/B testing was conducted separately for users playing between 30 and 500 rounds and the top 1% of players.

### Users Playing Between 30 and 500 Rounds

- **1-day Retention:** No statistically significant difference was observed.
- **7-day Retention:** A small but statistically significant increase of approximately 0.01 ppt.
- **Average Rounds Played:** A small but statistically significant increase of approximately 1 round.

### Top 1% of Users

- **1-day Retention:** No statistically significant difference was observed.
- **7-day Retention:** A small decrease of approximately 0.015 ppt, which may need further testing.
- **Average Rounds Played:** An increase of approximately 25 rounds, which may need further testing.

## Conclusion

For users playing between 30 and 500 rounds, the gate adjustment resulted in a small but statistically significant improvement in 7-day retention and average rounds played. However, for the top 1% of users, further investigation is needed to confirm observed changes. Overall, the gate adjustment appears to positively impact user engagement within specific segments, emphasizing the importance of segment-specific analysis in interpreting A/B testing results.
