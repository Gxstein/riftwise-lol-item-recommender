# Riftwise

**Context-aware item recommendations for League of Legends.**

Riftwise is a Python project exploring explainable item recommendations. Given a champion, lane, and opposing-team profile, the application is designed to rank suitable items and show the signals behind each suggestion.

## Project focus

- Build a small, patch-aware champion and item catalog.
- Use matchup context to rank candidate items.
- Explain recommendations in terms of item properties and explicit matchup rules.
- Evaluate behavior against documented scenarios.

The initial recommender uses transparent, deterministic rules. Its score is a ranking heuristic; it is not a win probability, a claim of optimality, or a trained machine-learning model.

## Current status

Initial development. The repository currently contains the project structure and technical documentation; the data catalog, recommendation engine, and interface are being developed.

## Technology

- Python
- Streamlit
- JSON for the initial local catalog
- Git and GitHub

## Data and policy

Champion and item metadata will come from Riot's [Data Dragon](https://developer.riotgames.com/docs/lol), with the data patch recorded in the repository. Riftwise does not rely on an OP.GG API or automated scraping.

Before distributing a player-facing product, review and comply with the applicable [Riot developer policies](https://support-developer.riotgames.com/hc/en-us/articles/22698698001939-League-of-Legends).

## Documentation

- [Architecture and diagrams](docs/ARCHITECTURE.md)
- [Technical decisions](docs/DECISIONS.md)

## Disclaimer

Riftwise is an independent project and is not affiliated with Riot Games, League of Legends, OP.GG, or Blitz. Their names and marks belong to their respective owners.
