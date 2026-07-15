# 00 — Methodik und Datengrundlage

## 1. Warum die erste Analyse ersetzt werden musste

Die erste Fassung war sorgfältiger als ein gewöhnliches GitHub-Profil, hatte aber vier systematische Fehler:

1. **Unvollständige Stichprobe.** Sie sah nur einen Teil der öffentlichen Repositories und konnte zentrale private Repos wie CATCHIT, ANVIL, CUE-AGENT, MIXTRACT, GAIME oder RAPIER nicht auswerten.
2. **Code = Kompetenz.** Sie leitete aus Repository-Sprachen direkte persönliche Sprachkompetenz ab. In einem agentisch erzeugten Portfolio ist das nicht zulässig.
3. **Aktivität = Leistungsfähigkeit.** Commitzahlen und Repo-Größen wurden zu stark gewichtet.
4. **README-Claims = Realität.** Teilweise wurden beschriebene Funktionen, Produktionsreife und Architektur als implementiert behandelt, ohne Beweisstufe und Reifegrad sauber zu trennen.

Version 2 behält die gute Grundidee der Triangulation, ändert aber die Einheit der Analyse.

Nicht mehr:

> Sprache + Commits + Repo-Größe → Kompetenz

Sondern:

> Wiederkehrende Entscheidungsmuster + konkrete Verträge + ausführbare Artefakte + Test/Gate-Evidenz + Prozessspuren + Gegenhypothesen → vorsichtige Kompetenzinferenz

## 2. Datengrundlage

### 2.1 Verbundener GitHub-Zugang

Die Analyse nutzt den mit ChatGPT verbundenen GitHub-Zugang für `Lootziffer666`. Dadurch waren öffentliche und zugängliche private Repositories, Dateien und ausgewählte Pull-Request-Verläufe sichtbar.

Vertieft geprüft wurden insbesondere:

- CATCHIT
- ANVIL
- ANVIL-CLIENT
- ANVIL-BELLOWS
- CUE-AGENT
- MIXTRACT
- RAPIER
- GAIME
- LAUNCHPAD
- KIDS_LAUNCHER
- DESIGN_SYSTEM
- WIZARD
- SWIFT
- SHADED
- TRIVIUM
- MYTHIC

Zusätzlich wurde die hochgeladene erste Analyse als Vergleichs- und Ausgangsdokument ausgewertet.

### 2.2 Sichtbarkeitsgrenze

Ein privates Repo kann eine Kompetenz intern stark belegen, ist aber **kein öffentlich prüfbarer Portfolio-Beweis**. Deshalb werden zwei Ebenen getrennt:

- **Analyse-Evidenz:** Für die interne Einschätzung zugänglich.
- **Portfolio-Evidenz:** Für Dritte ohne Sonderzugriff prüfbar.

CATCHIT ist derzeit eines der stärksten Analyse-Artefakte, benötigt aber für ein öffentliches Portfolio ein redigiertes Evidence Bundle mit Screenshots, Spezifikationsauszügen und anonymisierten Testresultaten.

## 3. Evidenzstufen

| Stufe | Bezeichnung | Mindestanforderung | Zulässige Aussage |
|---|---|---|---|
| **E4** | Operativ belegt | ausführbarer Pfad plus Tests/Gates/strukturierte Outputs oder nachvollziehbare PR-Evidenz | „wurde umgesetzt und geprüft“ |
| **E3** | Strukturell stark | konkrete Verträge, Zustände, Invarianten und wiederholte Implementationsspuren | „ist als belastbares Systemdesign belegt“ |
| **E2** | Teilimplementiert | kohärentes Design und erkennbare Teile, aber fehlender End-to-End-Beweis | „ist plausibel und teilweise realisiert“ |
| **E1** | Behauptet | README, Plan oder Konzept ohne ausreichenden Umsetzungsbeleg | „ist vorgesehen/beschrieben“ |
| **E0** | Nicht belegbar | keine prüfbare Spur oder widersprüchliche Angaben | keine Kompetenzbehauptung |

## 4. Beitragsarten statt Sprachratings

Für agentisch entwickelte Software werden vier Beitragsarten verwendet:

| Kürzel | Beitrag | Beispiele |
|---|---|---|
| **H** | menschliche semantische Autorschaft | Problemdefinition, Kanon, Zustände, Prioritäten, UX-Entscheidungen, Akzeptanz |
| **A** | Agentenimplementierung | erzeugter Code, Refactorings, Tests, Dokumententwürfe |
| **J** | gemeinsame Orchestrierungsleistung | Prompt-/Vertragsschleifen, Review, Korrektur, Integration, Merge-Entscheidung |
| **U** | unklar | aus dem Artefakt nicht sauber zuzuordnen |

Die Repos belegen das Ergebnis. Die genaue Zeile-für-Zeile-Urheberschaft lässt sich aus Git allein nicht rekonstruieren. Deshalb wird keine manuelle Syntaxkompetenz behauptet, wo sie nicht separat nachgewiesen ist.

## 5. Prüfschema pro Kompetenzclaim

Jeder starke Claim muss sechs Fragen überstehen:

1. **Was ist direkt beobachtbar?**
2. **Welche persönliche Leistung ist daraus ableitbar?**
3. **Welche alternative Erklärung gibt es?**
4. **Ist das Muster in mehreren unabhängigen Projekten sichtbar?**
5. **Welche Evidenzstufe erreicht es?**
6. **Was darf ausdrücklich nicht daraus geschlossen werden?**

## 6. Wissenschaftlich belastbare Leitplanken

Die Analyse verwendet Forschung nur als Grenze der Interpretation, nicht als wissenschaftlichen Glitzer.

### SPACE Framework

Forsgren et al. zeigen, dass Entwicklerproduktivität nicht auf eine einzelne Dimension oder Metrik reduziert werden kann. Commit-, PR- und Reviewzahlen sind Aktivitätsindikatoren, keine isolierten Leistungsmaße.

Konsequenz für dieses Portfolio:

- Commitzahlen werden nicht als Skillscore verwendet.
- Aktivität wird nur im Kontext von Qualität, Ergebnis, Kollaboration und Flow interpretiert.
- Unsichtbare Arbeit wie Architektur, Spezifikation und Review wird ausdrücklich berücksichtigt.

Quelle: [The SPACE of Developer Productivity, ACM Queue, 2021](https://queue.acm.org/detail.cfm?id=3454124)

### DevEx Framework

Noda et al. verdichten Developer Experience auf Feedback Loops, Cognitive Load und Flow State. Diese drei Dimensionen sind für Christians Portfolio besonders relevant, weil viele Projekte Werkzeuge bauen, die Kontextwechsel, manuelle Schritte und unklare Rückmeldungen reduzieren.

Konsequenz:

- „Friction reduction“ wird nicht als leere Markenformel behandelt.
- Es wird geprüft, ob ein Repo tatsächlich Feedback beschleunigt, kognitive Last senkt oder einen Arbeitsfluss erhält.

Quelle: [DevEx: What Actually Drives Productivity, ACM Queue, 2023](https://queue.acm.org/detail.cfm?id=3595878)

### Grenzen von Repository Mining

Kuutila et al. zeigen, dass Repositoryvariablen individuelle Produktivität und Wohlbefinden nur eingeschränkt vorhersagen; individuelle Unterschiede dominieren.

Konsequenz:

- Keine psychologischen Diagnosen aus GitHub.
- Keine Aussage „506 Commits beweisen hohe Produktivität“.
- Keine Rangliste anhand von Aktivitätszahlen.

Quelle: [Individual Differences Limit Predicting Well-being and Productivity Using Software Repositories, Empirical Software Engineering, 2021](https://doi.org/10.1007/s10664-021-09977-1)

### AI-unterstützte Entwicklung

Aktuelle Forschung beschreibt AI-Werkzeuge eher als Augmentation als als vollständigen Ersatz; der Nutzen hängt stark von Aufgabe, Person, Prozess und organisatorischer Einbettung ab.

Konsequenz:

- Agentennutzung entwertet die Arbeit nicht automatisch.
- Sie verschiebt aber die nachzuweisende Kompetenz von Syntaxproduktion zu Zielmodellierung, Steuerung, Review und Systemintegration.
- Codevolumen darf noch weniger als zuvor mit menschlicher Leistung gleichgesetzt werden.

Quelle: [The SPACE of AI: Real-World Lessons on AI's Impact on Developers, 2025](https://arxiv.org/abs/2508.00178)

## 7. Was diese Analyse leisten kann

Sie kann belastbar zeigen:

- welche Arten von Problemen wiederholt gewählt werden,
- wie Systeme semantisch geschnitten werden,
- ob Zustände, Verträge und Grenzen konsistent modelliert sind,
- wie Agentenarbeit kontrolliert und geprüft wird,
- welche UX- und Governance-Prinzipien wiederkehren,
- welche Projekte operativ, strukturell oder nur konzeptionell belegt sind.

Sie kann nicht beweisen:

- wie viel Code manuell geschrieben wurde,
- wie schnell Christian ohne Agenten programmieren könnte,
- wie er in einem klassischen Entwicklerteam arbeitet,
- ob Produkte im Markt skalieren,
- ob Nutzer zufrieden sind,
- ob ein System unter produktiver Last stabil bleibt.

## 8. Vertrauensregel

> Je größer der Claim, desto direkter muss der Beweis sein.

Eine starke Portfoliofassung zeigt daher nicht möglichst viele Fähigkeiten, sondern **wenige präzise Claims mit dichtem Beweisnetz**.
