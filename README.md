# QuiQui: Wettfahrtregeln Segeln

Fragen für Live-Abstimmungen mit [QuiQui](https://github.com/th-nuernberg/quiqui) zu den **Wettfahrtregeln Segeln 2025–2028** (DSV/World Sailing), gedacht für Kurse und Seminare für Wettfahrtleiter und Wettfahrtkomitees.

Das Repo folgt dem Format von [quiqui-questions](https://github.com/th-nuernberg/quiqui-questions): Fragen als YAML-Dateien, Sitzungseinstellungen in `config.yaml`.

## Fragedateien

| Datei | Thema | Fragen | Bezug |
|---|---|---|---|
| `00-vorbereitungsfragen.yaml` | Verständnisfragen aus dem Vorbereitungsfragebogen des Bayerischen Segelverbands für den Grundkurs Wettfahrtleiter: Beginn der Wettfahrt, Änderung der Segelanweisungen, Startstrafen, Rückrufsignale, Bahnverkürzung | 5 | Definitionen, Regeln 26, 29, 30, 32, 90.2 |
| `01-start-und-signale.yaml` | Start und Signale: Zeitnahme, Vorbereitungssignale, Verschiebung, Allgemeiner Rückruf, I-Flaggen-Regel | 5 | Regeln 26–30, Wettfahrtsignale |
| `02-ziel-wertung.yaml` | Ziel, Zeitlimit und Wertung: Durchs-Ziel-Gehen, Wettfahrtzeitlimit, Wertung bei Aufgabe oder Disqualifikation, Wertungsabkürzungen | 5 | Definitionen, Regel 35, Anhang A |
| `config.yaml` | QuiQui-Sitzung (`session_url`, `title`, `shuffle`) | | |

## Aufbau einer Frage

Jede Frage ist ein Eintrag mit `question`, `type` (`single` oder `multiple`) und `answers`. Alle Fragen sind bewertet:

- `correct` nennt die richtige(n) Antwort(en) und ist nur für den Host sichtbar (Schaltfläche „Reveal").
- `explanation` ist der Lösungshinweis für den Host. Er nennt die maßgebliche Regel mit Nummer und begründet, warum die übrigen Antworten falsch sind.
- Wo Flaggen eine Rolle spielen, sind sie als Abbildungen eingebunden, auch gestapelt (z. B. AP über A). Die Bilder stammen von Wikimedia Commons und werden per URL geladen.

## Verwenden

1. In QuiQui auf der Host-Seite „From GitHub" wählen, die Adresse dieses Repos eintragen und eine Datei auswählen.
2. Die Teilnehmer treten per QR-Code oder über den Join-Link der `session_url` aus `config.yaml` bei.

## Hinweise

- Die Lösungen und Hinweise sind aus dem deutschen Text der Wettfahrtregeln 2025–2028 hergeleitet und ohne Gewähr. Sie sind keine amtliche Auslegung.
- Die Fragen in `00-vorbereitungsfragen.yaml` stammen im Wortlaut aus dem Fragebogen des Bayerischen Segelverbands. Die Lösungen dazu hat der Fragebogen nicht vorgegeben; sie sind hier ergänzt.
- Der Regeltext selbst ist urheberrechtlich geschützt und nicht Teil dieses Repos.
