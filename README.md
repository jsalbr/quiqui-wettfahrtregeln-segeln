# QuiQui: Wettfahrtregeln Segeln

Fragen für Live-Abstimmungen mit [QuiQui](https://github.com/th-nuernberg/quiqui) zu den **Wettfahrtregeln Segeln 2025–2028** (DSV/World Sailing), gedacht für Kurse und Seminare für Wettfahrtleiter und Wettfahrtkomitees.

Das Repo folgt dem Format von [quiqui-questions](https://github.com/th-nuernberg/quiqui-questions): Fragen als YAML-Dateien, Sitzungseinstellungen in `config.yaml`.

## Inhalt

| Datei | Zweck |
|---|---|
| `config.yaml` | QuiQui-Sitzung: `session_url`, `title`, `shuffle` |
| `01-vorbereitungsfragen.yaml` | Fünf Verständnisfragen aus dem Vorbereitungsfragebogen des Bayerischen Segelverbands (Grundkurs für Wettfahrtleiter), mit Flaggen von Wikimedia Commons; unbewertete Abstimmung |
| `tools/extract_regeln.py` | Skript, das aus dem Regel-PDF den deutschen Text als Markdown extrahiert |
| `CLAUDE.md` | Entscheidungen und Konventionen für die Arbeit an diesem Repo |

Lokal vorhanden, aber nicht im Git (siehe `.gitignore`):

- `DSV_Wettfahrtregeln_deutsch_englisch-2025_2028.pdf` und `Vorbereitungsfragen.pdf`: Quelldokumente
- `dsv-wettfahrtregeln/`: deutscher Regeltext als Markdown, nach Teilen getrennt, mit erhaltenen Regelnummern

## Verwenden

1. Repo auf GitHub öffentlich halten (QuiQui lädt nur öffentliche Repos unter 1 MB).
2. Auf der QuiQui-Host-Seite „From GitHub" wählen, die Repo-URL eintragen, eine Fragen-Datei auswählen.
3. Teilnehmer treten über den QR-Code bzw. `/join/<session_url>` bei. Die `session_url` steht in `config.yaml` und sollte nach dem ersten Einsatz nicht mehr geändert werden.

Alternativ lässt sich eine einzelne Datei lokal per „From file" laden. Dann braucht sie einen eigenen `config:`-Block, siehe `self-contained-example.yaml` in quiqui-questions.

## Regeltext neu erzeugen

Voraussetzungen: Python 3 und `pdftohtml` (poppler).

```
python3 tools/extract_regeln.py DSV_Wettfahrtregeln_deutsch_englisch-2025_2028.pdf dsv-wettfahrtregeln cache.xml
```

Der Regeltext unterliegt dem Urheberrecht der DSV bzw. von World Sailing und wird deshalb nicht im Repo veröffentlicht.

## Fragensammlungen und Quellen

Eine deutschsprachige, öffentlich abrufbare Sammlung von Übungs- oder Prüfungsfragen für Wettfahrtleiter habe ich nicht gefunden. Die folgenden Quellen waren zuletzt abrufbar (Stand 11.10.2026) und taugen als Themen- und Stilvorlage. Sie beziehen sich auf die Regeln 2021–2024; Antworten müssen gegen die Regeln 2025–2028 geprüft werden.

**Fragen**

- [US Sailing: Basic Race Management Study Questions (2021)](https://www.ussailing.org/wp-content/uploads/2021/04/BRMS-Study-Questions-2021.pdf): englisch, 9 Seiten Multiple-Choice zu Veranstalter, Wettfahrtkomitee und Segelanweisungen; Regelverweis jeweils zum Ausfüllen, ohne Lösungen.
- [World Sailing: Racing Rules Question and Answer Service (Stand 30. April 2021)](https://sailing.org/tools/documents/2021booklet210430-[27262].pdf): englisch, 24 Seiten Frage-Antwort-Szenarien von Race Officials, nach Regelabschnitt geordnet. Die Antworten sind keine verbindlichen Auslegungen.

**Hintergrund (keine Fragen)**

- [ÖSV: Richtlinien für Wettfahrtleiter](https://segelverband.at/fileadmin/user_upload/oesv-web/Dokumente-Website/Dokumente_-_Regatten/Dokumente-RO-Wettfahrtleiter/richtlinien_des_oesv_fuer_wettfahrtleiter.pdf)
- [Swiss Sailing: Tag der Offiziellen 2025, Änderungen der Regeln (deutsch)](https://swiss-sailing.ch/_Resources/Persistent/4/5/b/1/45b144406be0815381f7728c5f97ffa41a199767/TdO25_Changes_RRS_DE.pdf)
- [Sail Canada: 2021–2024 Rule Changes for Race Officers](https://www.sailing.ca/wp-content/uploads/2022/11/2021-2024-Rule-Changes-for-Race-Officers-1.pdf)
- [Yachting NZ: Race Management Seminar](https://www.yachtingnz.org.nz/sites/default/files/2019-04/Race%20Management%20Seminar.pdf)

Die Fragensammlungen sind urheberrechtlich geschützt; sie dienen hier als Vorlage, die Fragen in diesem Repo sind eigene Formulierungen bzw. stammen aus dem genannten BSV-Fragebogen.
