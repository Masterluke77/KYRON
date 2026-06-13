# KYRON

**KYRON** ist eine Multi-Sport Prediction & Scouting Intelligence Platform.

KYRON ist nicht nur eine Fußball-Tippmaschine. Football ist das erste Sportmodul, aber der Core wird sportneutral, stream-aware und langfristig für viele Sportarten gebaut.

## Ziel

KYRON soll Wahrscheinlichkeiten berechnen, Simulationen ausführen, Scouting-Profile erzeugen, Datenqualität überwachen, Modellversionen auditieren, User-Tipps verwalten, Reports erzeugen und später Ads/Sponsoring sowie API-/White-Label-Nutzung vorbereiten.

## Start-Deployment

Primär:

- NAS / Docker / Portainer
- lokale Vollversion

Später:

- Hetzner VPS
- Coolify
- Staging/Production

Nicht vorgesehen:

- All-Inkl Shared Hosting
- PHP-Bastellösung
- Vercel-/AWS-Zwang
- harte lokale Pfade

## Tech Stack

Frontend:

- Next.js
- React
- TypeScript
- Tailwind CSS
- shadcn/ui
- Recharts oder ECharts
- i18n-ready
- PWA-ready

Backend:

- Python
- FastAPI
- SQLAlchemy
- Alembic
- Pydantic
- RBAC/Permissions

Data/Worker:

- PostgreSQL
- Redis
- RQ oder später Celery
- pandas/numpy/scipy/scikit-learn optional

## Wichtigster Grundsatz

Die Prediction Engine entscheidet. Die KI erklärt nur.

Keine KI darf Wahrscheinlichkeiten erfinden oder Modellwerte überschreiben.

## Erste Entwicklungsaufgabe

Siehe:

- `docs/KYRON_CODEX_TASKS.md`
- `docs/KYRON_MVP_ROADMAP.md`
- `AGENTS.md`
