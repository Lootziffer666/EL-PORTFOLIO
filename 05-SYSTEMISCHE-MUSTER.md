# 05 — Systemische Muster

Die wichtigste Evidenz entsteht nicht durch ein einzelnes Projekt, sondern durch **wiederkehrende Entscheidungen in unabhängigen Domänen**. Ein Muster gilt hier als stark, wenn es in mindestens drei Repositories mit konkreten Artefakten auftaucht.

## Muster 1 — Meaning before implementation

### Beobachtung

- CATCHIT trennt Live Truth, Structural Contract und Decision Lock.
- TRIVIUM übersetzt Bedeutung über eine WIR statt Quellsyntax direkt umzuschreiben.
- ANVIL definiert Artefaktverträge zwischen spezialisierten Engines.
- MIXTRACT trennt das, was analysiert wurde, von dem, was tatsächlich extrahiert wurde.

### Inferenz

Christian denkt Software nicht zuerst als Funktionsliste, sondern als **Bedeutungsvertrag**. Die Implementation darf diesen Vertrag ausführen, aber nicht still verändern.

### Beruflicher Wert

- weniger Missverständnisse zwischen Produkt und Technik,
- bessere Delegierbarkeit an Agenten,
- klarere Test- und Reviewkriterien,
- geringere semantische Drift bei Iterationen.

## Muster 2 — No silent fallback

### Beobachtung

- CATCHIT verbietet stille Fallbacks in der State Machine.
- CUE-AGENT nutzt Strict Mode und Exitcodes.
- TRIVIUM signalisiert Human Review explizit.
- MIXTRACT markiert defekte oder nur analytische Pfade.
- MYTHIC überspringt abhängige Deployments nach Upstream-Fehlern statt Erfolg vorzutäuschen.

### Inferenz

Fehler werden als **sichtbare Zustände** modelliert, nicht als kosmetisch verdeckte Abweichung.

### Beruflicher Wert

Das ist besonders relevant für AI-Systeme, weil generierte Software häufig plausibel klingt, obwohl Inputs, Ausgaben oder Integrationen falsch sind.

## Muster 3 — Contracted modularity

### Beobachtung

- ANVIL ist Control Plane, nicht Engine.
- SWIFT erzeugt Manifeste; SHADED konsumiert Actor-/Asset-Verträge.
- TRIVIUM besitzt Source/WIR/Target-Schichten.
- ANVIL-BELLOWS kapselt Provider, Modelle, Budget und Routing.

### Inferenz

Modularität wird nicht als Verzeichnisstruktur verstanden, sondern als **explizite Übergabeverantwortung**.

### Beruflicher Wert

- Komponenten können ersetzt werden,
- Agenten erhalten kleinere Verantwortungsräume,
- Fehler lassen sich lokalisieren,
- ein Update soll nicht das gesamte Ökosystem semantisch brechen.

## Muster 4 — Evidence over claims

### Beobachtung

- CUE-AGENT verlangt Evidence Bundles.
- CATCHIT-Gates verlangen Befehle, Resultate und Screenshots.
- SWIFT liefert maschinenlesbare Manifeste und Exitcodes.
- TRIVIUM führt Verlustinformationen.
- MIXTRACT dokumentiert genaue Ausgabepfade und Diagnostik.

### Inferenz

Der Akzeptanzzustand wird durch **prüfbare Artefakte** definiert, nicht durch die Aussage „fertig“.

### Beruflicher Wert

Diese Fähigkeit ist zentral für agentische Teams, in denen Geschwindigkeit ohne Beweis leicht zu unsichtbarer technischer Schuld wird.

## Muster 5 — UX is state, not screens

### Beobachtung

- CATCHIT organisiert Verhalten über Zustände und Dringlichkeitsachsen.
- LAUNCHPAD reduziert Navigationsmöglichkeiten durch Kiosklogik.
- KIDS_LAUNCHER setzt Controller-first und Eltern-Gate.
- DESIGN_SYSTEM koppelt Komponenten an semantische Tokens statt feste Farben.

### Inferenz

Oberflächen werden als **begehbarer Zustandsraum** entworfen. Layout folgt Bedeutung und Handlungsdruck.

### Beruflicher Wert

- weniger kognitive Last,
- klarere nächste Aktion,
- bessere Recovery,
- konsistente Interaktion über visuelle Varianten hinweg.

## Muster 6 — Frictionless control surfaces

### Beobachtung

- MYTHIC reduziert Deployment auf einen geführten Produktfluss.
- RAPIER verlegt Agentensteuerung in Sprache.
- ANVIL-CLIENT bündelt Cockpit, Audit und BYOK.
- ANVIL-BELLOWS vereinheitlicht Provider- und Budgetsteuerung.

### Inferenz

Christian sucht wiederholt den Punkt, an dem ein technisch mächtiger Prozess für Menschen **unnötig fragmentiert** wird, und baut eine kontrollierende Komfortschicht darüber.

### Anschluss an DevEx-Forschung

Das entspricht den DevEx-Dimensionen:

- schnellere Feedback Loops,
- geringere extrinsische kognitive Last,
- weniger Kontextwechsel und damit besserer Flow.

## Muster 7 — Recombination across domains

### Beobachtung

Dieselben Ideen wandern zwischen Mobilität, Game-Entwicklung, Audio, Deployment und Agentensteuerung:

- State Machines,
- Gates,
- Evidence Envelopes,
- Manifeste,
- kanonische Begriffe,
- Review-Exits,
- Recovery-Zustände.

### Inferenz

Die Innovationsleistung liegt oft nicht in einer völlig neuen Einzeltechnik, sondern darin, **ein wirksames Prinzip aus einem Kontext in einen anderen zu übertragen**, ohne seine Funktion zu verlieren.

## Muster 8 — Human as semantic end filter

### Beobachtung

Das gesamte Arbeitsmodell setzt voraus, dass Agenten generieren dürfen, aber nicht selbst bestimmen, was wahr oder akzeptabel ist.

### Inferenz

Christian übernimmt die Rolle des **semantischen Endfilters**:

- Was trifft die Absicht?
- Was fühlt sich systemfremd an?
- Welche Abkürzung zerstört den Kern?
- Welche Agentenantwort ist plausibel, aber falsch?
- Welcher Zustand muss kanonisch werden?

Diese Rolle ist schwer über klassische Code-Metriken zu erfassen, aber in Verträgen, Abweisungen, Revisionen und repoübergreifender Konsistenz sichtbar.

## Gesamtformel

```text
Frictionless Systems
= Meaning Model
+ Explicit State
+ Bounded Agents
+ Evidence Gates
+ Human Canon
```

Das ist die konsistenteste Beschreibung des Portfolios.
