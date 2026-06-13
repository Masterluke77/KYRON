# KYRON ARCHITECTURE

## 1. Architekturziel

KYRON wird als modularer Multi-Service-Stack gebaut:

- Web App
- API
- Worker
- PostgreSQL
- Redis
- Storage
- optional Reverse Proxy

## 2. Services

### kyron-web

Next.js App für:

- Public App
- User Area
- Admin Center

### kyron-api

FastAPI Backend für:

- Auth
- Core Domain
- Admin APIs
- User APIs
- Prediction APIs
- Scouting APIs
- Reports
- Ads
- Theme/i18n

### kyron-worker

Worker für:

- Data Imports
- Prediction Runs
- Simulation Runs
- Accuracy Jobs
- Backtests
- Reports
- Data Quality Checks
- Scouting Jobs

### kyron-postgres

Hauptdatenbank.

### kyron-redis

Queue, Cache, Jobstatus.

## 3. Repository-Struktur

```text
kyron/
├─ apps/
│  ├─ web/
│  └─ api/
├─ packages/
│  ├─ shared-types/
│  └─ ui-contracts/
├─ infra/
├─ storage/
├─ docs/
├─ docker-compose.yml
├─ .env.example
├─ README.md
└─ AGENTS.md
```

## 4. Backend-Modulstruktur

```text
apps/api/app/
├─ main.py
├─ core/
├─ db/
├─ auth/
├─ modules/
│  ├─ sports/
│  ├─ competitions/
│  ├─ events/
│  ├─ participants/
│  ├─ predictions/
│  ├─ simulations/
│  ├─ scouting/
│  ├─ datahub/
│  ├─ ads/
│  ├─ theme/
│  ├─ i18n/
│  ├─ reports/
│  ├─ audit/
│  └─ admin/
├─ workers/
└─ tests/
```

## 5. Frontend-Modulstruktur

```text
apps/web/
├─ app/
├─ components/
├─ features/
├─ lib/
├─ i18n/
├─ themes/
└─ public/
```

## 6. Core-Prinzip

Core ist sportneutral.

Sportlogik liegt in Adaptern/Modulen.

## 7. Data Flow

1. Datenquelle liefert Daten
2. Data Hub importiert
3. Data Quality prüft
4. Event/Participants werden aktualisiert
5. Data Snapshot wird erstellt
6. Prediction Engine rechnet
7. Prediction wird gespeichert
8. Explain Engine erzeugt Erklärung
9. UI/API zeigt Ergebnis
10. Ergebnis kommt später rein
11. Accuracy bewertet Prediction
12. Model Lab erkennt Verbesserungspotenzial

## 8. Keine Blockierung im Request

Schwere Arbeiten laufen im Worker:

- Prediction Bulk
- Simulation
- Backtest
- Report-Erzeugung
- Data Import
- Accuracy Recalculation
