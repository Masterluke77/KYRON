# KYRON PREDICTION ENGINE

## 1. Grundsatz

KYRON berechnet Wahrscheinlichkeiten, nicht Bauchgefühl-Tipps.

Die Prediction Engine entscheidet.
Die KI erklärt nur.

## 2. Prediction Pipeline

1. Event auswählen
2. Sportart und Stream erkennen
3. Prediction Target bestimmen
4. Sportmodul laden
5. Datenqualität prüfen
6. Data Snapshot erstellen
7. Features berechnen
8. aktive Modellversion laden
9. Modellfamilien berechnen
10. Ensemble berechnen
11. Output validieren
12. Confidence und Risk bestimmen
13. Prediction speichern
14. Components speichern
15. Change Log erzeugen
16. Explanation Payload erzeugen
17. Audit schreiben

## 3. Data Quality Gate

Status:

- EXCELLENT
- GOOD
- PARTIAL
- STALE
- CONFLICTING
- MISSING
- UNKNOWN

Keine produktive Prediction ohne ausreichende Datenqualität, außer Low-Data Mode ist markiert.

## 4. Model Families

- ELO
- POISSON
- XG
- FORM
- MARKET_SIGNAL
- MATCHUP
- PARTICIPANT_IMPACT
- CONTEXT
- ML_CLASSIFIER
- SIMULATION
- ENSEMBLE

## 5. Baseline First

Jede Sportart startet mit robustem Baseline-Modell.

Football V1:

- Elo Basic
- Form Basic
- Poisson Basic
- Weighted Ensemble

## 6. Output

Jede Prediction enthält:

- probabilities
- expected values
- confidence_score
- risk_level
- data_quality_score
- components
- explanation_payload
- model_version
- data_snapshot
- generated_at

## 7. Evaluation

Nach Ergebnis:

- Prediction Evaluation
- Brier Score
- Log Loss
- Hit Rate
- Calibration
- Target-specific metrics

## 8. Learning

KYRON lernt kontrolliert:

1. Measurement
2. Diagnosis
3. Recommendation
4. Backtesting
5. Candidate Model
6. Admin Approval
7. Rollout
8. Monitoring
9. Rollback

Kein aktives Modell darf still ersetzt werden.

## 9. Low-Data Mode

Erlaubt, aber immer klar markieren.

Low-Data Predictions haben niedrigere Confidence und höhere Risk Flags.

## 10. Market Signal

Quoten sind nur Signal.

Keine Wettgarantie.
Keine direkte Kopie.
Kein Sponsoreneinfluss.
