# 12 — Wissenschaftliche Einordnung

## 1. Was „wissenschaftlich evidenzbasiert“ hier bedeuten darf

Eine GitHub-Analyse ist keine psychometrische Untersuchung und kein standardisiertes Kompetenzassessment. Wissenschaftliche Literatur kann:

- vor Fehlinterpretationen von Metriken warnen,
- geeignete Beobachtungsdimensionen liefern,
- Grenzen von Repository Mining erklären,
- qualitative und quantitative Beweise strukturieren.

Sie kann nicht aus Repositories beweisen, dass eine Person „hochintelligent“, „kreativ“, „senior“ oder „produktiv“ ist.

Die korrekte Form lautet daher:

> Die Artefakte zeigen wiederkehrende, beruflich relevante Verhaltens- und Entscheidungsmuster. Forschung begründet, warum diese multidimensional und kontextsensitiv bewertet werden müssen.

## 2. SPACE statt Commit-Score

Forsgren et al. unterscheiden fünf Dimensionen:

- Satisfaction and well-being,
- Performance,
- Activity,
- Communication and collaboration,
- Efficiency and flow.

Für dieses Portfolio ist wichtig:

- Commits, PRs und Reviews sind nur **Activity**.
- Design-Dokumente und Spezifikationen sind ebenfalls Aktivitätsartefakte, aber mit anderem Informationswert.
- Performance muss über Ergebnisqualität, Zuverlässigkeit und Wirkung geprüft werden.
- Flow zeigt sich hier vor allem in der Reduktion von Handoffs und Kontextwechseln.
- Collaboration umfasst im agentischen Kontext auch die Qualität der Mensch-Agent-Werkzeug-Koordination, darf aber nicht mit menschlicher Teamführung gleichgesetzt werden.

**Quelle:** Nicole Forsgren et al., [The SPACE of Developer Productivity](https://queue.acm.org/detail.cfm?id=3454124), ACM Queue 19(1), 2021, DOI 10.1145/3454122.3454124.

## 3. DevEx als passende Linse für Reibungsreduktion

Noda et al. identifizieren drei zentrale Dimensionen:

1. Feedback Loops,
2. Cognitive Load,
3. Flow State.

Christians Repos können entlang dieser Dimensionen gelesen werden:

| DevEx-Dimension | Portfolio-Beispiel |
|---|---|
| Feedback Loops | CUE-AGENT, Tests, Review-Bots, strukturierte Exitcodes |
| Cognitive Load | CATCHIT One-space Surface, Launcher, MYTHIC, ANVIL-CLIENT |
| Flow State | RAPIER, mobile Auftragsschicht, reduzierte Toolwechsel |

Das beweist keine gemessene DevEx-Wirkung. Es zeigt aber, dass die Produktprobleme systematisch auf bekannte Reibungsdimensionen zielen.

**Quelle:** Abi Noda et al., [DevEx: What Actually Drives Productivity](https://queue.acm.org/detail.cfm?id=3595878), ACM Queue 21(2), 2023.

## 4. Repository Mining ist laut Forschung unvollständig

Kuutila et al. verbanden Repositorydaten mit täglichen Selbstauskünften in einem industriellen Längsschnitt. Individuelle Unterschiede erklärten einen großen Teil der Varianz; Repositoryvariablen sagten Wohlbefinden und Produktivität nur begrenzt voraus.

Konsequenz:

- keine Produktivitätsdiagnose aus Commitfrequenz,
- keine persönliche Leistungsrangliste,
- keine psychologische Schlussfolgerung,
- qualitative Kontextdaten bleiben notwendig.

**Quelle:** Miikka Kuutila et al., [Individual Differences Limit Predicting Well-being and Productivity Using Software Repositories](https://doi.org/10.1007/s10664-021-09977-1), Empirical Software Engineering, 2021.

## 5. Produktivität und Qualität sind keine einfache Gegenrechnung

Storey, Houck und Zimmermann zeigen, dass Entwickler und Manager Produktivität unterschiedlich definieren und Qualität häufig als Robustheit verstehen. Die Wahrnehmung von Trade-offs variiert stark.

Für dieses Portfolio folgt daraus:

- Geschwindigkeit durch Agenten ist keine ausreichende Erfolgsmetrik.
- Qualitätsclaims müssen als konkrete Attribute formuliert werden: Robustheit, Wahrheit, Recovery, Nachvollziehbarkeit, Testbarkeit.
- „Mehr Output“ kann bei unkontrollierten Agenten sogar mehr Review- und Korrekturarbeit bedeuten.

**Quelle:** Margaret-Anne Storey, Brian Houck, Thomas Zimmermann, [How Developers and Managers Define and Trade Productivity for Quality](https://arxiv.org/abs/2111.04302), 2021.

## 6. AI ändert die Einheit der Arbeit

Die SPACE-of-AI-Studie berichtet, dass AI-Werkzeuge in realen Teams häufig Effizienz und Zufriedenheit für Routineaufgaben verbessern, die Wirkung jedoch stark von Aufgabe, Nutzungsmuster und organisatorischer Einbettung abhängt.

Für Christians Portfolio ist die vorsichtige Schlussfolgerung:

- AI-Nutzung ist weder automatischer Kompetenzbeweis noch automatische Entwertung.
- Die relevante Frage lautet, welche menschlichen Fähigkeiten nach der Syntaxautomatisierung übrig bleiben und sichtbar werden.
- Hier sind es Problemwahl, Semantik, Systemgrenzen, Kontrolle, Review und Akzeptanz.

**Quelle:** Brian Houck et al., [The SPACE of AI: Real-World Lessons on AI's Impact on Developers](https://arxiv.org/abs/2508.00178), 2025. Preprint; daher vorsichtig zu gewichten.

## 7. Triangulationsmodell für dieses Portfolio

Ein starker Kompetenzclaim benötigt mindestens drei voneinander verschiedene Beweisarten:

### Artefaktbeweis

- Spec,
- State Machine,
- Schema,
- Manifest,
- Gate-Konfiguration,
- ausführbarer Output.

### Prozessbeweis

- PR-Verlauf,
- Reviewdiskussion,
- Korrekturcommit,
- Konfliktauflösung,
- Versionierung.

### Ergebnisbeweis

- Testresultat,
- Screenshot,
- Video,
- Evidence Bundle,
- externe Nutzung,
- reproduzierbarer Demo-Run.

Zusätzlich braucht es eine Gegenhypothese:

> Könnte das Artefakt vollständig von einem Agenten erzeugt worden sein, ohne dass Christian die zugeschriebene Kompetenz besitzt?

Der Claim wird nur dann stark, wenn die wiederholte Auswahl, Korrektur und Integration über unabhängige Projekte die Gegenhypothese schwächt.

## 8. Wissenschaftlich saubere Schlussfolgerung

Die Repositories beweisen nicht klassische Programmierseniorität. Sie liefern jedoch **konvergierende qualitative Evidenz** für:

- systematische Bedeutungsmodellierung,
- Contract- und State-Design,
- agentische Arbeitszerlegung,
- evidenzbasierte Akzeptanz,
- Failure Honesty,
- reibungsorientierte UX-Architektur,
- systemübergreifende Rekombination.

Die Evidenz ist am stärksten, wo Spezifikation, Implementation, Gate und Prozessspur gemeinsam vorhanden sind — besonders bei CATCHIT, ANVIL/CUE-AGENT und den manifestbasierten Game-Pipelines.

## Literatur

1. Forsgren, N., Storey, M.-A., Maddila, C., Zimmermann, T., Houck, B., Butler, J. (2021). *The SPACE of Developer Productivity*. ACM Queue 19(1). DOI: 10.1145/3454122.3454124.
2. Noda, A., Storey, M.-A., Forsgren, N., Greiler, M. (2023). *DevEx: What Actually Drives Productivity*. ACM Queue 21(2).
3. Kuutila, M., Mäntylä, M., Claes, M., Elovainio, M., Adams, B. (2021). *Individual Differences Limit Predicting Well-being and Productivity Using Software Repositories*. Empirical Software Engineering. DOI: 10.1007/s10664-021-09977-1.
4. Storey, M.-A., Houck, B., Zimmermann, T. (2021). *How Developers and Managers Define and Trade Productivity for Quality*. arXiv:2111.04302.
5. Houck, B., Lowdermilk, T., Beyer, C., Clarke, S., Hanrahan, B. (2025). *The SPACE of AI: Real-World Lessons on AI's Impact on Developers*. arXiv:2508.00178. Preprint.
