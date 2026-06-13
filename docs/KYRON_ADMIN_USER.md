# KYRON ADMIN CENTER & USER AREA

## 1. Oberflächen

KYRON hat:

- Public App
- User Area
- Admin Center

## 2. Security

Grundsätze:

- deny by default
- least privilege
- serverseitige Permissions
- Audit für kritische Aktionen
- keine Admin-Sicherheit nur im Frontend

## 3. Rollen

Systemrollen:

- GUEST
- USER
- PREMIUM_USER
- SCOUT_PRO
- ANALYST
- DATA_MANAGER
- MODEL_MANAGER
- AD_MANAGER
- THEME_MANAGER
- REPORT_MANAGER
- ADMIN
- SUPER_ADMIN

## 4. Admin Center Routen

```text
/admin
/admin/sports
/admin/streams
/admin/competitions
/admin/seasons
/admin/events
/admin/participants
/admin/predictions
/admin/simulations
/admin/model-lab
/admin/accuracy
/admin/data-hub
/admin/data-quality
/admin/scouting
/admin/reports
/admin/ads
/admin/theme
/admin/i18n
/admin/users
/admin/roles
/admin/audit
/admin/jobs
/admin/logs
/admin/backups
/admin/settings
```

## 5. Admin Funktionen

Admin Center verwaltet:

- Sports & Streams
- Competitions
- Seasons
- Events
- Participants
- Results
- Predictions
- Simulations
- Model Lab
- Accuracy
- Data Hub
- Data Quality
- Scouting
- Reports
- Ads
- Theme
- i18n
- Users/Roles
- Jobs
- Logs
- Backups
- Audit

## 6. User Area Routen

```text
/app
/app/dashboard
/app/my-picks
/app/groups
/app/leaderboards
/app/watchlist
/app/favorites
/app/scout
/app/reports
/app/notifications
/app/profile
/app/privacy
/app/settings
```

## 7. User Funktionen

User können:

- eigene Tipps abgeben
- Tippgruppen nutzen
- Leaderboards sehen
- Kyron vs User vergleichen
- Watchlists nutzen
- Favoriten setzen
- Notifications verwalten
- Scouting Shortlists nutzen, je nach Plan
- Theme/Sprache/Zeitzone einstellen
- Consent/Privacy verwalten

## 8. Lock-Regel

User Picks sind nach Lock-Zeit nicht mehr änderbar.

Normalerweise Lock = Eventstart.

## 9. Ads/Prediction Trennung

Sponsor kann Placement kaufen.
Sponsor darf niemals Prediction oder Score beeinflussen.

## 10. Auditpflichtige Aktionen

- Modell aktivieren
- Modell zurückrollen
- Ergebnis ändern
- Participant mergen
- Datenquelle deaktivieren
- Ads Kampagne aktivieren
- Theme aktivieren
- Rolle/Recht ändern
- Backup löschen
