# AGENTS.md — KYRON Development Rules

Diese Regeln sind für Codex und alle Entwickler verbindlich.

## 1. Arbeitsmodus

Arbeite wie ein Senior-Architekt, Backend-Entwickler, Frontend-Entwickler, UI/UX-Designer und Qualitätsprüfer.

Keine Bastellösungen.
Keine halben Features.
Keine stillen Architekturänderungen.
Keine ungeprüften Abkürzungen.

## 2. Absolute Produktregeln

KYRON ist:

- Multi-Sport
- Multi-Stream
- Event-basiert
- Participant-basiert
- Prediction-versioniert
- Model-versioniert
- Data-Snapshot-basiert
- Scouting-ready
- Ads-ready
- Theme-ready
- i18n-ready
- PWA-ready
- Audit-ready
- Docker-first
- Local-first

Football ist nur das erste Sportmodul, nicht der Core.

## 3. Harte Verbote

Du darfst nicht:

- eine zentrale `matches`-Tabelle als Core bauen
- Football hart im Core verdrahten
- Männer/Frauen als einfachen Textfilter behandeln
- unterschiedliche Streams in Ratings oder Modellen mischen
- Prediction-Historie überschreiben
- Modellversionen weglassen
- Data Snapshots weglassen
- Wahrscheinlichkeiten durch ein LLM erzeugen lassen
- User Picks direkt als Modelltraining verwenden
- Businesslogik ins Frontend legen
- Admin-Rechte nur im Frontend prüfen
- kritische Aktionen ohne Audit bauen
- Secrets in Code oder Repo schreiben
- lokale Festpfade hart codieren
- UI-Texte hart codieren
- Farben hart codieren
- Mobile/Responsive ignorieren
- i18n ignorieren
- Theme Tokens ignorieren
- Ads ohne Consent-Struktur bauen
- Sponsoreneinfluss auf Predictions oder Scores erlauben

## 4. Architekturregeln

Core verwendet neutrale Begriffe:

- sports
- streams
- competitions
- seasons
- events
- participants
- prediction_targets
- predictions
- model_versions
- data_snapshots
- simulations
- ratings
- scouting_profiles
- reports
- ads
- audit_logs

Sportlogik gehört in Sportmodule:

- football
- tennis
- basketball
- racing
- esports
- combat
- golf
- darts
- snooker
- cycling

## 5. Stream-Regel

Alle Sportarten werden stream-getrennt behandelt.

Globale Streams:

- MEN
- WOMEN
- YOUTH_MEN
- YOUTH_WOMEN
- MIXED
- OPEN
- PARA
- JUNIOR_OPEN
- SENIOR
- CUSTOM

Ratings, Modelle, Benchmarks, Scouting, Accuracy und Simulationen müssen stream-getrennt sein.

## 6. Prediction-Regel

Jede Prediction braucht:

- sport_id
- stream_id
- competition_id
- season_id
- event_id
- prediction_target_id
- model_version_id
- data_snapshot_id
- predicted_at
- output_payload
- confidence_score
- risk_level
- data_quality_score

Alte Predictions werden nie überschrieben.

## 7. KI-Regel

Die KI darf:

- erklären
- zusammenfassen
- Reports formulieren
- Risikoanalyse textlich darstellen
- Admin-Hinweise formulieren

Die KI darf nicht:

- Wahrscheinlichkeiten erfinden
- Modellwerte ändern
- fehlende Daten halluzinieren
- sichere Wettversprechen formulieren

## 8. UI-Regeln

Alle UI muss sein:

- responsive
- theme-token-basiert
- multilingual vorbereitet
- barrierearm
- mobile nutzbar
- desktop-stark
- statusklar
- nicht nur über Farbe verständlich

Keine harten Farben. Keine harten Texte. Keine Hover-only Bedienung.

## 9. Security-Regeln

Nutze:

- deny by default
- least privilege
- serverseitige Permissions
- Audit für kritische Aktionen
- sichere Passwortspeicherung
- keine Secrets im Repo
- .env.example statt echter .env
- Input Validation
- restriktive CORS-Konfiguration

## 10. Definition of Done

Ein Feature ist erst fertig, wenn:

- Backend implementiert ist
- Frontend implementiert ist, falls UI nötig
- DB Migration vorhanden ist
- Permissions geprüft sind
- Audit geprüft ist, falls kritisch
- i18n Keys vorhanden sind
- Theme Tokens genutzt werden
- Responsive Verhalten geprüft ist
- Fehlerfälle behandelt sind
- Tests oder Testnotizen vorhanden sind
- Dokumentation aktualisiert ist
- keine Secrets enthalten sind
