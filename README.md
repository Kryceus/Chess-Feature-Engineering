# Chess Performance Analytics

A data analytics tool that identifies chess weaknesses for any player by analysing their recent games from Chess.com or Lichess.

## What it does
- Fetches games automatically from Chess.com or Lichess API by username
- Analyses every board position across multiple games
- Measures 4 tactical and positional features per move
- Correlates each weakness with actual loss rate
- Produces a ranked weakness report showing which patterns cost the player the most games

## Features measured
- **Hanging pieces** — how often the player leaves pieces unprotected
- **Failed to protect** — how often the player ignores threats made by the opponent
- **Underdevelopment** — how often pieces remain on starting squares past move 10
- **Centre control** — how often the opponent has more pieces in the central squares

## Example output

=== TOP WEAKNESSES FOR username ===

Failed to protect: 80% loss rate when worse than opponent
Hanging pieces: 73% loss rate when worse than opponent
Weaker middle: 71% loss rate when worse than opponent
Underdeveloped: 50% loss rate when worse than opponent

## Tech stack
- Python
- python-chess
- Pandas
- Requests
- Google Colab

## Limitations and future improvements
- Does not account for opening theory when measuring development
- Correlation metrics depend on sample size — more games gives more reliable results
- Future: add Stockfish centipawn loss as ground truth label
- Future: cluster players by weakness pattern across a database of users
