# 02 — Autorschaft und Rollenprofil

## 1. Warum eine Urheberschaftserklärung notwendig ist

In einem traditionellen Portfolio wird stillschweigend angenommen:

> Wer das Repo besitzt, hat den Code geschrieben.

Bei AI-assisted Development ist diese Annahme falsch. Ein ehrliches Portfolio muss mindestens vier Ebenen unterscheiden:

1. **Wer hat das Problem gewählt?**
2. **Wer hat die Bedeutung und Grenzen definiert?**
3. **Wer hat die konkrete Implementierung erzeugt?**
4. **Wer hat entschieden, ob das Ergebnis akzeptabel ist?**

Bei Christian liegen Problemwahl, semantische Architektur, Produktentscheidungen und finale Akzeptanz überwiegend beim Menschen; große Teile der Syntaxproduktion liegen bei Coding-Agenten.

## 2. Das belastbare Autorschaftsmodell

### Christian verantwortet primär

- Problemframing und Zielzustand,
- Nutzer- und Stresskontext,
- Produktkanon und Namenssystem,
- Zustände, Übergänge und Invarianten,
- Scope und explizite Nicht-Ziele,
- Rollenverteilung zwischen Repositories und Agenten,
- Akzeptanzkriterien, Kill-Gates und Beweisformate,
- Auswahl und Steuerung der Coding-Agenten,
- Priorisierung von Bugs und Korrekturen,
- Integrations-, Merge- und Richtungsentscheidungen,
- die Frage, was als wahr, fertig oder gescheitert gilt.

### Coding-Agenten verantworten häufig

- konkrete Syntaxproduktion,
- Boilerplate und Projektgerüste,
- Implementierung abgegrenzter Features,
- Refactorings,
- Test- und Dokumententwürfe,
- mechanische Migrationen,
- Fehlerkorrekturen nach Reviewhinweisen.

### Review-Agenten und Werkzeuge liefern

- statische Analysen,
- potenzielle Defekte,
- Diff-Zusammenfassungen,
- Test- und CI-Rückmeldungen,
- Hinweise auf Inkonsistenzen,
- Review-Vorschläge.

### Die gemeinsame Leistung

Das Produkt entsteht aus einem Steuerkreis:

```text
Intent
  → Contract
    → Agent Implementation
      → Test / Review / Evidence
        → Human Judgment
          → Correction or Canon
```

Die relevante persönliche Kompetenz ist daher nicht „jede Zeile selbst geschrieben“, sondern **die Qualität dieses Steuerkreises**.

## 3. Was GitHub tatsächlich belegt

GitHub kann zeigen:

- dass definierte Zustände, Verträge und Gates existieren,
- dass Repos systematisch miteinander verbunden sind,
- dass PRs in mehreren Iterationen korrigiert werden,
- dass Reviewergebnisse in Änderungen einfließen,
- dass Claims mit strukturierten Evidence-Artifacts gekoppelt werden,
- dass dieselben Governance-Prinzipien wiederkehren.

GitHub kann nicht sicher zeigen:

- wer einen einzelnen Codeblock formuliert hat,
- wie viel Prompting oder Nacharbeit nötig war,
- ob der Nutzer eine Sprache ohne Hilfsmittel beherrscht,
- ob eine Architekturidee vollständig von Christian oder aus Agentenvorschlägen stammt.

Deshalb wird im CV auf **verantwortete Entscheidungen** statt auf ungeklärte Zeilenautorschaft fokussiert.

## 4. Empfohlene Berufsbezeichnungen

### 4.1 AI-assisted Product Builder

Die verständlichste Primärbezeichnung. Sie sagt:

- Christian baut echte Produkte und Prototypen,
- nutzt AI als Produktionsmittel,
- übernimmt Produkt- und Systemverantwortung,
- behauptet nicht, klassischer Hands-on-Coder zu sein.

### 4.2 Systems/UX Architect

Diese Bezeichnung ist durch die wiederkehrende Verbindung von Zustandslogik, Informationsarchitektur, Fehlersemantik und Oberflächenverhalten gedeckt.

Sie muss allerdings konkretisiert werden:

> Systems/UX Architect für meaning-first, agentisch implementierte Produkte.

### 4.3 Agentic Development Lead

Passend, wenn die Rolle nicht mit Personalführung verwechselt wird. Gemeint ist:

- Arbeitszerlegung für Agenten,
- Contract-first Delegation,
- Review- und Gate-Design,
- Agentenwahl und Eskalation,
- Integration und Freigabe.

Besserer Zusatz:

> Leads agentic development workflows, not a conventional engineering team.

### 4.4 Technical Product Owner

Gut anschlussfähig für Unternehmen. Der technische Anteil liegt in Systemgrenzen, Verträgen und Architekturentscheidungen, nicht in täglicher Syntaxarbeit.

## 5. Nicht geeignete Selbstbezeichnungen

### „Full-Stack Developer“

Zu unpräzise und irreführend. Die Repos enthalten viele Stacks, aber ihre bloße Existenz beweist keine eigenständige manuelle Beherrschung.

### „Software Architect“ ohne Zusatz

Kann Erwartungen an langjährige Produktions-, Team- und Betriebsverantwortung wecken. Besser: Product Systems Architect oder Systems/UX Architect.

### „Prompt Engineer“

Zu eng und zu schwach. Christians Arbeit besteht nicht im Formulieren hübscher Prompts, sondern in Produktkanon, Verträgen, Zuständen, Gatekeeping und Systemkomposition.

### „Vibe Coder“

Beschreibt das Werkzeug, nicht die Disziplin. Außerdem verschleiert der Begriff gerade das, was das Portfolio besonders macht: Kontrolle, Wahrheitsgrenzen und Beweisführung.

## 6. Portfolio-Autorschaftsstatement

Folgende Formulierung kann öffentlich verwendet werden:

> I design product meaning, system boundaries, state models, UX behavior, acceptance gates, and evidence requirements. Coding agents implement substantial parts of the source code under those constraints. I review outcomes, direct corrections, integrate components, and decide what becomes canonical. The portfolio therefore documents my product, systems, orchestration, and validation work—not unsupported claims of manual mastery in every language present in the repositories.

Deutsche Fassung:

> Ich definiere Produktbedeutung, Systemgrenzen, Zustandsmodelle, UX-Verhalten, Akzeptanz-Gates und erforderliche Beweise. Coding-Agenten implementieren wesentliche Teile des Quellcodes innerhalb dieser Vorgaben. Ich prüfe Ergebnisse, steuere Korrekturen, integriere Komponenten und entscheide, was kanonisch wird. Das Portfolio belegt daher meine Produkt-, System-, Orchestrierungs- und Validierungsarbeit — nicht eine unbelegte manuelle Beherrschung jeder im Repo vorkommenden Sprache.

## 7. Das eigentliche Senioritätssignal

Seniorität zeigt sich hier nicht primär an Syntax oder Jahren in einer Stellenbezeichnung, sondern an der Fähigkeit:

- Unklarheit zu lokalisieren,
- Konsequenzen vor der Implementierung sichtbar zu machen,
- Systeme gegen stille Bedeutungsverschiebung abzusichern,
- Agenten in begrenzte Verantwortungsräume zu setzen,
- Fehler als strukturierte Zustände statt als Überraschung zu behandeln,
- eine große Ideenlandschaft in austauschbare, kanonische Module zu schneiden.

Das ist ein reales Senioritätssignal — aber in einer neuen Rollenklasse, nicht als Ersatzbehauptung für klassische Engineering-Erfahrung.
