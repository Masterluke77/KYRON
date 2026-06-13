# KYRON MVP ROADMAP

## Release 0 — Foundation Skeleton

Ziel:

- Monorepo
- Docker Compose
- Next.js Web
- FastAPI API
- PostgreSQL
- Redis
- Worker
- Healthchecks
- .env.example

## Release 1 — Core Domain

- sports
- streams
- sport_streams
- competitions
- seasons
- stages
- groups
- venues
- events
- participants
- event_participants
- event_results
- users
- roles
- permissions
- audit_logs

## Release 2 — Theme + i18n + Responsive Shell

- Theme Provider
- Design Tokens
- Dark/Light
- High Contrast vorbereitet
- DE/EN
- Public/User/Admin Shell
- Mobile Navigation
- Status Badges

## Release 3 — Data Hub Basic

- data_sources
- coverage
- import_jobs
- import_errors
- data_quality_checks
- CSV/JSON Import Basis
- Manual Entry

## Release 4 — Football Module Basic

- Football Extension
- Football Men/Women getrennt
- Football Prediction Targets
- Turnierstruktur
- Gruppen
- Spielplan
- Ergebnisse

## Release 5 — Prediction Engine Basic

- prediction_targets
- model_families
- model_versions
- feature_sets
- data_snapshots
- predictions
- components
- Football Baseline
- Elo/Form/Poisson/Ensemble

## Release 6 — Results + Accuracy Basic

- prediction_evaluations
- model_metrics
- Brier Score
- Log Loss
- Hit Rate
- Calibration Basic

## Release 7 — Simulation Basic

- simulation_runs
- simulation_results
- Group Simulation
- Tournament Winner Simulation

## Release 8 — User Area Basic

- Login
- User Dashboard
- User Picks
- Watchlists
- Groups
- Leaderboards
- Notifications
- Settings

## Release 9 — Scouting Foundation

- rating_universes
- scouting_universes
- scouting_profiles
- scouting_metric_values
- league_strength_ratings
- shortlists
- scouting_reports

## Release 10 — Model Lab Basic

- model version management
- weight editor
- backtest runs
- candidate models
- approval flow
- rollback
- drift checks

## Release 11 — Reports Basic

- prediction reports
- simulation reports
- scouting reports
- PDF/JSON export
- report themes
- DE/EN

## Release 12 — Ads/Sponsorship Foundation

- sponsors
- campaigns
- placements
- creatives
- impressions
- clicks
- consent records
- privacy settings

## Release 13 — Backup, Betrieb, Qualität

- backup_runs
- stored_files
- healthchecks
- logs
- job status
- backup script
- restore README

## Codex Epic-Gruppen

Epic A: Foundation  
Release 0–2

Epic B: Data + Football  
Release 3–4

Epic C: Prediction + Accuracy + Simulation  
Release 5–7

Epic D: User + Scout  
Release 8–9

Epic E: Model Lab + Reports  
Release 10–11

Epic F: Monetization + Ops  
Release 12–13
