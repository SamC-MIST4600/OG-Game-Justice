# OG Game Justic

My app helps Game Studios decide which old games deserve continued developer support/ a remastered edition by sorting to games only order than 10 years than comparing ratings, playtime, revenue, and owners.

> A course project for **MIST 4600: Computer Programming in Business** at the University of Georgia's Terry College of Business (Fall 2026).

## Problem
Many Game Studios suffer from the issue of constrained resources. Studios only have so many developers and storage capacity, because of this many old games, despite their popularity, lose developer support. My app gives data insights that help Game Studios see which old games are still active using steam's data source. Without my app many Game Studios would be making operation decisions without concrete data. 

## What it does
My app answers three questions:
**1. Release_year:** How many games are more than 10 years old
**2. Ratings:** Of these games, what are the top ten by ratings?
**3. Playtime:** Of these games, what are the top ten by playtime?

## Data
The [Steam Games Dataset](https://www.kaggle.com/datasets/artermiloff/steam-games-dataset) on Kaggle, collected in March 2025. The dataset is shared under the MIT License by its creator, artermiloff. This repo uses `steam_games.csv`, a smaller file made for the course: the 1,000 games with the most reviews.

## Built with
- Python and pandas, in Google Colab
- Coming soon: my outside tool

## How to run it
Coming soon

## Example output
*Subquestion 2:* Of the games that are older than 10 years what are the top twenty by ratings?

def top_10_old_games(games):
    old_games = games[games["release_year"] < 2016]
    best = old_games.sort_values("pct_pos_total", ascending=False)
    return best[["name", "release_year", "pct_pos_total"]].head(20)

print(top_10_old_games(games))

## AI Use Disclosure
Coming soon

## Author
Sam C
