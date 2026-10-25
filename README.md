# R-Project-Video-Games-Sales

## About the Project

This project explores video game sales data using R to investigate relationships between commercial performance, critic ratings, game genres, platforms, publishers, and developers.

The analysis uses the Video Game Sales with Ratings dataset from Kaggle, which combines video game sales data from VGChartz with critic and user ratings from Metacritic.

The goal is to identify trends in the video game industry and examine whether review scores and game genres are associated with sales performance.

## Project Objectives
- Explore the distribution of video games across platforms, genres, publishers, developers, and age ratings.
- Analyze relationships between global sales, European sales, and critic scores.
- Investigate correlations between critic ratings and sales using Pearson and Spearman correlation tests.
- Evaluate the relationship between critic scores and global sales using linear regression.
- Compare sales distributions between Sports games and games from other genres using a t-test.

## Methodology

### 1. Data Loading and Preparation

- Import the dataset using readr.
- Inspect data structure, variable types, and summary statistics.
- Handle missing values and filter observations for specific analyses.

### 2. Exploratory Data Analysis (EDA)

- Use ggplot2 to visualize categorical and quantitative variables.
- Categorical variables: Examine game counts by platform, genre, publisher, developer, and rating.
- Quantitative variables: Explore distributions and relationships among global sales, critic scores, critic counts, and user counts.
- Scatterplots: Investigate the relationship between critic scores and global sales, with points colored by platform.
- Boxplots: Compare global sales distributions across genres.

### 3. Correlation Analysis

Apply Pearson and Spearman correlation tests to investigate associations between critic scores and sales.

| Variables                       | Pearson correlation | Spearman correlation |
|---------------------------------|--------------------:|---------------------:|
| Global Sales vs. Critic Score   | 0.237               | 0.383                |
| EU Sales vs. Critic Score       | 0.212               | 0.351                |

Both analyses indicate positive associations between critic scores and sales, with the Spearman correlations suggesting stronger monotonic relationships than the Pearson correlations.

### 4. Linear Regression

Fit a simple linear regression model to examine whether critic scores are associated with global sales.

- Independent variable: Critic Score
- Dependent variable: Global Sales
- R-squared: Approximately 0.06
- Statistical significance: p-value below 0.05

The model indicates a statistically significant positive relationship, but critic scores alone explain only a small proportion of the variation in global sales.

### 5. Hypothesis Testing

Use a two-sample t-test to compare mean global sales between Sports games and games from other genres, restricting the analysis to titles with global sales below one million.

The analysis found a statistically significant difference between the groups, with mean sales of approximately 0.349 million for Sports games and 0.280 million for other games in the filtered dataset.

## Key Findings

- Platform distribution: PlayStation 2 has the largest number of game records in the analyzed dataset.
- Genre distribution: Action is the most frequently represented genre, while Puzzle is the least frequent.
- Publishers and developers: Electronic Arts has the most published game records, while Ubisoft has the most developed game records.
- Ratings: E (Everyone) is the most common ESRB rating.
- Critic scores and sales: Higher critic scores tend to be associated with higher global and European sales, although the relationships are not strong.
- Genre comparison: Sports games have higher mean global sales than other genres within the selected subset, with a statistically significant difference.

## Technologies & Libraries
- R
- tidyverse
- ggplot2
- readr
- Statistical methods: Pearson correlation, Spearman correlation, linear regression, and two-sample t-tests

## Dataset
Source: Video Game Sales with Ratings — Kaggle (https://www.kaggle.com/datasets/rush4ratio/video-game-sales-with-ratings).

The dataset contains video game sales figures alongside critic scores, user ratings, platform information, genres, publishers, developers, and ESRB ratings.
