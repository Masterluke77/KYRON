# KYRON CODEX QUICK GUIDE FÜR MARKUS

## 1. Kurz gesagt

Codex ist dein KI-Entwickler.

Du gibst Codex nicht:

```text
Mach alles.
```

Sondern:

```text
Mach genau Task 0.
Dann Task 1.
Dann Task 2.
```

## 2. So startest du

1. GitHub Repo `kyron` erstellen
2. Dieses Paket ins Repo hochladen
3. Codex öffnen
4. GitHub verbinden
5. Repo `kyron` auswählen
6. Codex diesen Satz geben:

```text
Bitte lies zuerst AGENTS.md, README.md und alle Dateien im docs-Ordner. Halte dich strikt daran. Keine Architektur eigenmächtig ändern. Keine Features löschen. Keine Abkürzungen.
```

## 3. Erster Auftrag an Codex

Kopiere aus `docs/KYRON_CODEX_TASKS.md` den Abschnitt:

```text
TASK 0 — Foundation Skeleton
```

und gib ihn Codex.

## 4. Danach prüfen

Wenn Codex fertig ist, prüfst du:

- Hat er Dateien gelöscht?
- Hat er die Planung ignoriert?
- Gibt es Secrets?
- Startet Docker?
- Antwortet API `/health`?
- Läuft die Web-App?
- Hat er unnötig Football eingebaut?
- Hat er Texte/Farben hart codiert?

## 5. Wenn alles gut ist

Dann:

- Änderungen übernehmen
- committen
- nächsten Task geben

## 6. Goldene Regel

Immer nur ein Task.

Nicht hetzen.
Nicht alles auf einmal.

## 7. Standard-Satz für jeden Codex-Auftrag

```text
Halte dich strikt an AGENTS.md und die KYRON-Dokumente. Keine Architekturänderungen ohne Begründung. Keine Features entfernen. Keine Abkürzungen. Arbeite nur an dieser Aufgabe.
```

## 8. Wenn Codex Mist baut

Dann schreiben:

```text
Stop. Prüfe deine Änderungen gegen AGENTS.md. Entferne alles, was nicht zur Aufgabe gehört. Stelle gelöschte Planungsdateien wieder her. Keine Architekturänderungen.
```

## 9. Was du niemals ins Repo legst

- echte Passwörter
- API Keys
- Tokens
- echte Kundendaten
- private Zugangsdaten
- .env mit echten Werten

Nur `.env.example`.
