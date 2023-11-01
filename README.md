# IS445_Final_Project

# NBA Player Statistics Dataset

## Dataset Overview
The dataset represents individual NBA player statistics for multiple seasons.

## Fields/Columns
- `Rk`: Player rank.
- `Player`: Player's name.
- `Pos`: Player's position on the field (e.g., PG for Point Guard).
- `Age`: Player's age.
- `G`: Number of games played by the player in the season.
- `TRB`: Total rebounds.
- `AST`: Assists.
- `STL`: Steals.
- `BLK`: Blocks.
- `PTS`: Points scored.
- `Season`: The NBA season for which the stats are recorded (last two digits).
- `MVP`: Boolean value indicating whether the player was the Most Valuable Player for the season.
- `Player Score`: A derived score based on given statistics and weights.

## Data Types
- Numeric fields: `Rk`, `Age`, `G`, `TRB`, `AST`, `STL`, `BLK`, `PTS`, and `Player Score`.
- String fields: `Player`, `Pos`, and `Season`.
- Boolean fields: `MVP`.

## Data Characteristics
- The data spans multiple seasons, allowing for time series analysis.
- Players may appear multiple times if they have played in multiple seasons.
- The dataset is well-suited for analyzing player performance, comparing players, and identifying trends over time.

## Exploration Summary
- We filtered the dataset to focus on seasons from 2008-09 onwards.
- We combined stats for players who played for multiple teams in the same season.
- We derived a new metric, `Player Score`, to determine the best player for each season.

## Player Score Formula
The Player Score is derived using the following weighted formula:

Player Score = alpha * PTS + beta * TRB + gamma * AST + delta * STL + epsilon *BLK


Where the weights are defined as:
- (alpha) (for PTS): 1.5
- (beta) (for TRB): 2
- (gamma) (for AST): 2
- (delta) (for STL): 3
- (epsilon) (for BLK): 3


Misktake Score = alpha * TOV + beta * PF


Where the weights are defined as:
- (alpha) (for PTS): 10
- (beta) (for TRB): 15

## FINAL VISUALIZATION INDIVIDUAL
-In IS445_Li_Luwei_Individual.ipynb file, I did the data cleaning of the NBA_Player_Stats_2.csv, gather the useful information such as TRB, AST, STL, BLK, PTS, Season, TOV, PF in order to apply my formula to calculate the best player of the year.
My dataframe has player score, TRB, AST, STL, BLK, PTS, TOV, PF

## FINAL VISUALIZATION PEERS
-In IS445_Li_Luwei_Peers.ipynb file, I created a Radar Plot of the best player's stats in season 2020, 2021, 2022. The stats are including STL, AST, TRB, BLK, and PTS

## FINAL VISUALIZATION GENERAL PUBLIC
-In IS445_Li_Luwei_General_Public.ipynb file, I created a Radar Plot of the Positive Score (attack score) and negative score (mistake score) of the best players in season 2020, 2021, 2022. 
the Attack Score is showing public that the player's attack effeiency, the higher the better. 
the Mistake Score is showing public that how often player make mistakes, the higher the worse. 


