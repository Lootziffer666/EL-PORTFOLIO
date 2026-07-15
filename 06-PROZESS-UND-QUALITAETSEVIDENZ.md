# 06 — Prozess- und Qualitätsevidenz

## 1. Warum der Prozess wichtiger ist als Commitzahl

Die erste Analyse hob rund 500 Commits hervor. Das ist Aktivität, aber keine Qualitätsaussage. In agentischen Workflows können große Änderungen sehr schnell entstehen; dadurch steigt sogar die Bedeutung von Review, Begrenzung und Beweisführung.

Die relevantere Frage lautet:

> Gibt es Spuren, dass generierte Ergebnisse geprüft, korrigiert und gegen einen stabilen Vertrag gehalten werden?

Bei CATCHIT und den Governance-Repos lautet die Antwort: ja.

## 2. Pull-Request-Evidenz aus CATCHIT

Der sichtbare Verlauf erreicht mindestens PR #79 und zeigt mehrere Arten von Arbeit:

### Architekturiteration

- [PR #79](https://github.com/Lootziffer666/CATCHIT/pull/79): datengetriebene Storyboard-/Journey-Architektur.
- [PR #78](https://github.com/Lootziffer666/CATCHIT/pull/78): Ersatz einer Step-Machine durch ein 14-State-UI-Modell.
- [PR #77](https://github.com/Lootziffer666/CATCHIT/pull/77): neues Surface-Modul und state-driven UI.

**Interpretation:** Zustandsarchitektur wurde nicht einmal dokumentiert und dann vergessen, sondern in mehreren Implementationswellen konkretisiert.

### Konsistenzaudit

- [PR #70](https://github.com/Lootziffer666/CATCHIT/pull/70): Dokumentations- und Decision-Lock-Audit; mehrere Widersprüche wurden systematisch beseitigt.
- [PR #72](https://github.com/Lootziffer666/CATCHIT/pull/72): gefrorene Zustände, Validatoren und Tests.

**Interpretation:** Es gibt aktive Pflege kanonischer Wahrheit, nicht nur Feature-Anhäufung.

### Integration und Konfliktkorrektur

- [PR #73](https://github.com/Lootziffer666/CATCHIT/pull/73): Credentials, Geocoding, Provider, Tests und Konfliktauflösung.

**Interpretation:** Der Prozess enthält reale Integrationsreibung. Entscheidend ist nicht, dass Konflikte auftreten, sondern dass doppelte oder widersprüchliche Implementierung erkannt und korrigiert wird.

## 3. Review-Bots richtig interpretieren

CodeRabbit, Gemini, Kilo oder andere Reviewer sind keine unabhängigen menschlichen Gutachter. Ihre Kommentare beweisen nicht automatisch Codequalität.

Sie belegen jedoch:

- dass Diffs maschinell überprüft werden,
- dass Warnungen und Inkonsistenzen sichtbar gemacht werden,
- dass der Nutzer Reviewresultate als weitere Datenquelle nutzt,
- dass Agenten nicht allein über den Erfolg ihrer eigenen Arbeit urteilen.

Die persönliche Kompetenz liegt in:

- Auswahl der relevanten Kritik,
- Erkennen falscher oder systemfremder Vorschläge,
- Priorisierung,
- Formulierung des Korrekturvertrags,
- Prüfung, ob die Korrektur die eigentliche Bedeutung erhält.

## 4. Gate-Evidenz

### CATCHIT

`GATES.md` macht Freigabe von verbindlichen Checks, kritischen Privacy-/Security-Gates und Screenshot-Proofs abhängig. Ein Release darf nur stattfinden, wenn alle Pflichtprüfungen bestehen.

### CUE-AGENT

CUE-AGENT definiert:

- strukturierte JSON-Zusammenfassung,
- Strict Mode,
- eindeutige Exitcodes,
- Evidence-Verzeichnis,
- Validierungspipeline.

### SWIFT/TRIVIUM

Beide Systeme nutzen maschinenlesbare Ausgaben und explizite Exit-/Reviewzustände. Damit kann die nächste Pipeline-Stufe unterscheiden zwischen:

- Erfolg,
- technisch erzeugtem, aber semantisch unsicherem Ergebnis,
- notwendiger Human Review,
- echtem Fehler.

## 5. Qualitätskompetenz, die dadurch belegt ist

### Stark belegt

- Akzeptanzkriterien operationalisieren,
- Wahrheit und Status maschinenlesbar machen,
- Review- und Korrekturschleifen führen,
- Dokumente gegen Kanon prüfen,
- Integrationsrisiken sichtbar machen,
- Agentenclaims nicht ungeprüft übernehmen.

### Nur teilweise belegt

- vollständige Testabdeckung,
- systematische Mutation-/Property-Tests über alle Repos,
- langfristige Regression-Sicherheit,
- Last- und Performance-Tests,
- Security Audits durch Dritte.

## 6. Prozessrisiken

Die PR-Historie zeigt auch Schwächen, die im Portfolio nicht versteckt werden sollten:

### Hohe Änderungsrate

Viele große PRs in kurzer Zeit können Reviewkapazität überfordern. Ein Reviewer-Rate-Limit ist kein Produktivitätspreis, sondern ein Warnsignal: Die Beweis- und Korrekturschicht muss mit der Generierungsgeschwindigkeit wachsen.

### Agentische Branch-Namen und Titel

Automatisch erzeugte Namen sind intern praktisch, wirken öffentlich aber unprofessionell und verschleiern die eigentliche Entscheidung. Für Flagship-Repos sollten PR-Titel nachträglich kuratiert oder über Release Notes zusammengeführt werden.

### Dokumentation kann der Implementation vorauslaufen

Das Portfolio ist besonders dokumentationsstark. Deshalb muss jedes Dokument sichtbar zwischen `implemented`, `verified`, `partial`, `planned` und `aspirational` unterscheiden.

### Merge ist kein Beweis

Ein gemergter PR beweist nur Akzeptanz in den Branch, nicht reale Funktion. Evidence Bundles, Tests, Screenshots und reproduzierbare Demos sind höher zu gewichten.

## 7. Empfohlener agentischer Qualitätskreislauf

```text
1. Canonical contract
2. Small bounded task
3. Agent implementation
4. Automated tests
5. Independent review agent
6. Evidence bundle
7. Human semantic review
8. Merge or rejection
9. Post-merge smoke proof
10. Update evidence ledger
```

## 8. Portfolio-Claim

> Runs AI-assisted development as a governed review system: bounded tasks, explicit contracts, independent review signals, evidence gates, and human semantic acceptance.

Das ist stärker und ehrlicher als „schreibt sehr viel Code“.
