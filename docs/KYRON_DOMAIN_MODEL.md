# KYRON DOMAIN MODEL

## 1. Core-Begriffe

KYRON Core kennt:

- Sports
- Streams
- Competitions
- Seasons
- Stages
- Groups
- Events
- Participants
- Event Participants
- Results
- Prediction Targets
- Predictions
- Model Versions
- Data Snapshots
- Ratings
- Simulations
- Scouting Profiles
- Reports
- Ads
- Users
- Audit Logs

## 2. Sports

Sportarten sind globale Kategorien.

Beispiele:

- FOOTBALL
- TENNIS
- BASKETBALL
- RACING
- ESPORTS
- COMBAT_SPORTS

## 3. Streams

Streams gelten für alle Sportarten:

- MEN
- WOMEN
- YOUTH_MEN
- YOUTH_WOMEN
- MIXED
- OPEN
- PARA
- CUSTOM

## 4. Competitions

Eine Competition gehört immer zu:

- sport
- stream
- region/country optional
- organization optional

Beispiele:

- FIFA World Cup Men
- FIFA Women’s World Cup
- ATP Tour
- WTA Tour
- NBA
- WNBA
- Formula 1 Open

## 5. Events statt Matches

Core verwendet `event`.

Ein Event kann sein:

- Fußballspiel
- Tennismatch
- Basketballspiel
- Rennen
- Golfturnier
- Boxkampf
- E-Sports-Match

## 6. Participants statt Teams/Players

Core verwendet `participant`.

Ein Participant kann sein:

- Team
- Player
- Driver
- Fighter
- Club
- National Team
- Duo
- Squad
- Constructor
- E-Sports Team

## 7. Prediction

Eine Prediction gehört immer zu:

- Sport
- Stream
- Competition
- Season
- Event
- Prediction Target
- Model Version
- Data Snapshot

## 8. Ratings

Ratings werden in Rating Universes getrennt.

Beispiele:

- football_men_senior
- football_women_senior
- tennis_men_senior
- tennis_women_senior

## 9. Scouting

Scouting wird über Scouting Universes getrennt.

Kein Score ohne Universe.

## 10. Ads/Sponsoring

Ads sind eigenes Modul.

Werbung darf Predictions und Scores nie beeinflussen.

## 11. Theme/i18n

Theme und Sprache sind Plattformfunktionen, keine UI-Nachträge.
