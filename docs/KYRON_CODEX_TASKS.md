# KYRON CODEX TASKS

## Allgemeine Codex-Regel

Jede Aufgabe muss klein genug sein, um geprüft werden zu können.

Nie schreiben:

```text
Bau Kyron komplett.
```

Immer schreiben:

```text
Baue Release X mit klaren Akzeptanzkriterien.
```

---

# TASK 0 — Foundation Skeleton

## Ziel

Erzeuge ein lauffähiges Monorepo mit:

- Next.js Web-App unter `apps/web`
- FastAPI Backend unter `apps/api`
- PostgreSQL
- Redis
- Worker-Grundstruktur
- docker-compose.yml
- .env.example
- Healthchecks
- einfache Kyron Landing Shell
- API `/health`
- README mit Startanleitung

## Kontext

Lies zuerst:

- AGENTS.md
- README.md
- docs/KYRON_MASTERPLAN.md
- docs/KYRON_ARCHITECTURE.md
- docs/KYRON_MVP_ROADMAP.md

## Nicht anfassen

- keine Prediction-Logik
- keine Scouting-Logik
- keine Ads-Logik
- keine Sportlogik
- keine komplexe UI

## Akzeptanzkriterien

- `docker compose up` startet alle Services
- Web-App ist erreichbar
- API `/health` antwortet
- PostgreSQL läuft
- Redis läuft
- Worker startet
- keine Secrets im Repo
- `.env.example` ist vollständig
- Projektstruktur ist sauber und modular

## No-Go

- keine hart codierten Secrets
- keine lokalen Festpfade
- keine Football-Logik im Core
- keine unnötigen Abhängigkeiten
- keine Planungsdateien löschen

---

# TASK 1 — Core Domain Models

## Ziel

Implementiere Core-Domain-Tabellen und Basismodelle:

- sports
- competition_streams
- sport_streams
- countries
- organizations
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

## Akzeptanzkriterien

- Alembic Migration vorhanden
- SQLAlchemy Models vorhanden
- Pydantic Schemas vorhanden
- Admin Seed User vorbereitet
- Seed-Daten für Sports/Streams vorhanden
- Stream-Mismatch wird serverseitig verhindert oder für später als klarer Validator vorbereitet

## No-Go

- keine zentrale `matches`-Tabelle
- keine Football-Hardcodierung im Core
- keine Männer/Frauen-Vermischung

---

# TASK 2 — Theme/i18n/Responsive Shell

## Ziel

Erstelle die Grund-Shell für Public, User und Admin.

## Enthält

- Theme Provider
- Design Tokens
- Kyron Dark
- Kyron Light
- i18n Setup DE/EN
- Public Layout
- User Layout
- Admin Layout
- Mobile Navigation
- Status Badges

## Akzeptanzkriterien

- Sprache umschaltbar
- Theme umschaltbar
- keine hart codierten Farben in Hauptkomponenten
- keine hart codierten Texte in Hauptnavigation
- Mobile Layout bricht nicht

---

# TASK 3 — Data Hub Basic

## Ziel

Baue Datenquellen- und Import-Grundlage.

## Enthält

- data_sources
- data_source_coverage
- data_import_jobs
- data_import_errors
- data_quality_checks
- data_quality_results
- einfache CSV/JSON Import-Struktur

---

# TASK 4 — Football Module Basic

## Ziel

Baue Football als erstes Sportmodul, ohne Core zu verschmutzen.

## Enthält

- football_event_details
- football_lineups vorbereitet
- Football Prediction Targets
- Football Men/Women getrennt
- Seed-Daten für Beispielturnier

---

# TASK 5 — Prediction Engine Basic

## Ziel

Baue erste versionierte Prediction Engine.

## Enthält

- prediction_targets
- model_families
- model_versions
- data_snapshots
- predictions
- prediction_components
- Football Baseline Elo/Form/Poisson/Ensemble

## No-Go

- keine LLM-Wahrscheinlichkeiten
- keine Prediction ohne Model Version
- keine Prediction ohne Data Snapshot
- keine Prediction überschreiben

---

# TASK 6 — Accuracy Basic

## Ziel

Bewerte Predictions nach Ergebnissen.

## Enthält

- prediction_evaluations
- model_metrics
- Brier Score
- Log Loss
- Hit Rate
- Calibration Basic

---

# TASK 7 — Simulation Basic

## Ziel

Baue Football-Gruppen-/Turniersimulation.

## No-Go

- keine Simulation im API-Request blockierend
- Simulation muss Worker Job sein

---

# TASK 8 — User Area Basic

## Ziel

User können tippen, Watchlists nutzen und Statistiken sehen.

## No-Go

- User Picks dürfen Prediction Engine nicht verändern
- Picks nach Lock nicht änderbar

---

# TASK 9 — Scouting Foundation

## Ziel

Baue Scouting-Grundlage.

## No-Go

- kein Score ohne Scouting Universe
- keine Männer/Frauen-Benchmarkmischung

---

# TASK 10 — Model Lab Basic

## Ziel

Baue Modellverwaltung mit Backtest, Approval und Rollback.

## No-Go

- kein aktives Modell still überschreiben
- kein Rollout ohne Audit

---

# TASK 11 — Reports Basic

## Ziel

Baue Reports mit Datenstand, Modellversion, Sprache und Theme.

---

# TASK 12 — Ads Foundation

## Ziel

Baue Ads/Sponsorship-Grundlage mit Consent.

## No-Go

- Ads beeinflussen keine Predictions
- keine personalisierte Werbung ohne Consent

---

# TASK 13 — Ops/Backups

## Ziel

Baue Health, Logs, Backups und Restore-Dokumentation.
