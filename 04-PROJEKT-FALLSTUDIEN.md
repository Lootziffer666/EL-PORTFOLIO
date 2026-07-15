# 04 — Projekt-Fallstudien

## Leseregel

Jede Fallstudie trennt:

- Problem,
- persönlich zurechenbare Systementscheidung,
- Agenten-/Implementationsanteil,
- Beweis,
- Gegenhypothese,
- legitimen Portfolio-Claim,
- nicht legitimen Claim.

---

# Fallstudie 1 — CATCHIT

## Problem

ÖPNV-Apps liefern Daten, aber Menschen müssen unter Zeitdruck entscheiden: Ist die Verbindung noch machbar? Kann ich warten? Muss ich laufen? Was passiert nach einem verpassten Anschluss? Unsichere Echtzeitdaten und wechselnde UI-Seiten erhöhen die Belastung genau dann, wenn Orientierung gebraucht wird.

## Systementscheidung

CATCHIT wird als **meaning-first mobility MVP** modelliert. Zentrale Entscheidungen:

- One-space Surface statt klassischer Seitenhierarchie,
- getrennte Achsen für Datenvertrauen, Machbarkeit, Dringlichkeit, Recovery und Konsequenz,
- kanonische Zustandsmaschine statt verteilter UI-If-Logik,
- Decision Lock als explizites Datenobjekt,
- Trennung von Live Truth und Structural Contract,
- keine stillen Fallbacks,
- Gates und Screenshot-Beweise als Freigabebedingung.

Die State-Machine-Spezifikation führt 42 kanonische Zustände sowie Guards, Übergänge, Persistenzregeln und Invarianten.

## Persönlicher Beitrag

- Problemdefinition aus der Perspektive realer Mobilitätsbelastung,
- semantische Achsen und Zustände,
- Definition dessen, was die App behaupten darf,
- Recovery- und Konsequenzlogik,
- UX- und Gate-Verträge,
- Korrekturschleifen über zahlreiche PRs.

## Agentenanteil

- Implementierung von Modulen und UI-Zuständen,
- Tests und Refactorings,
- Dokumentationsentwürfe,
- technische Korrekturen nach Review.

## Beweise

- [CATCHIT README](https://github.com/Lootziffer666/CATCHIT/blob/main/README.md) — Architektur, Decision Lock, Route Engine, Live/Structural Truth.
- [State Machine Spec](https://github.com/Lootziffer666/CATCHIT/blob/main/docs/CATCHIT_STATE_MACHINE_SPEC_v1.md) — Zustände, Guards, Transitionen, Invarianten.
- [GATES.md](https://github.com/Lootziffer666/CATCHIT/blob/main/GATES.md) — harte Checks und Screenshot-Evidence.
- PR-Verlauf bis mindestens [PR #79](https://github.com/Lootziffer666/CATCHIT/pull/79) — wiederholte Architektur- und UI-Iterationen.
- [PR #70](https://github.com/Lootziffer666/CATCHIT/pull/70) — Konsistenzaudit gegen Decision Locks.
- [PR #72](https://github.com/Lootziffer666/CATCHIT/pull/72) — gefrorene Zustände und Validatoren.

## Evidenzstufe

**E4** für State-/Gate-/Contract-Design.  
**E3** für reale Nutzerwirksamkeit, solange keine systematische Feldstudie vorliegt.

## Legitimer Claim

> Defined and directed a 42-state, contract-driven mobility decision system that separates live-data confidence from structural truth and prevents silent UX fallbacks.

## Nicht legitimer Claim

> Built a production-proven transit platform used at scale.

---

# Fallstudie 2 — ANVIL + CUE-AGENT

## Problem

Coding-Agenten können schnell große Mengen Code und Erfolgsmeldungen erzeugen. Das Kernproblem ist nicht Generierung, sondern Kontrolle: Welche Engine ist zuständig? Welche Artefakte müssen existieren? Wie wird aus „sieht fertig aus“ ein prüfbarer Zustand?

## Systementscheidung

ANVIL ist als **Control Plane** für spezialisierte Generatoren ausgelegt, ausdrücklich nicht als monolithische Engine. Es orchestriert deterministische Artefaktverträge und delegiert Domänenarbeit an spezialisierte Komponenten.

CUE-AGENT ist der Gatekeeper: Spielbarkeit und Integrität werden über strukturierte Evidence Bundles, strikten Modus und Exitcodes geprüft — nicht über Behauptungen eines Agenten.

## Persönlicher Beitrag

- Trennung von Control Plane und Engines,
- Rollen- und Verantwortungsgrenzen,
- Idee des Artefaktvertrags als gemeinsame Sprache,
- Definition von Evidence statt Claim,
- Gatekeeper- und TRON-Prinzip,
- mobile/voice-orientierte Steuerungsvision.

## Agentenanteil

- CLI-, Adapter- und UI-Implementierung,
- Testgerüste,
- Dokumentation und Integrationscode.

## Beweise

- [ANVIL README](https://github.com/Lootziffer666/ANVIL/blob/main/README.md) — Control Plane, Nicht-Ziele, Integration Bible, Phasen.
- [CUE-AGENT README](https://github.com/Lootziffer666/CUE-AGENT/blob/main/README.md) — Evidence Bundle, Strict Mode, Exitcodes, Validation Pipeline.
- [ANVIL-CLIENT README](https://github.com/Lootziffer666/ANVIL-CLIENT/blob/main/README.md) — Cockpit, BYOK, Audit-/Artifact-Schicht.
- [ANVIL-BELLOWS README](https://github.com/Lootziffer666/ANVIL-BELLOWS/blob/main/README.md) — Provider-Routing, Budget- und Gate-Schicht.

## Evidenzstufe

**E4/E3** für Governance- und Evidenzarchitektur.  
**E2/E3** für das gesamte End-to-End-Ökosystem, solange nicht jede Engine in einem öffentlichen reproduzierbaren Lauf verbunden ist.

## Legitimer Claim

> Designed an agentic development control plane in which specialized generators must produce deterministic artifacts and pass evidence-based gates before their output is accepted.

## Nicht legitimer Claim

> Created a fully autonomous software factory that reliably builds any application.

---

# Fallstudie 3 — TRIVIUM

## Problem

Game-Assets und Spielbedeutung sind eng an Engines, Dimensionen und Genres gebunden. Syntaxkonvertierung allein erhält keine Spielmechanik, räumliche Bedeutung oder ästhetische Funktion.

## Systementscheidung

TRIVIUM übersetzt **Bedeutung statt Syntax**. Eine World Intermediate Representation (WIR) bildet den semantischen Zwischenraum. Verlustinformationen und Human-Review-Zustände werden explizit ausgegeben; Exitcode 2 signalisiert erforderliche menschliche Prüfung.

## Persönlicher Beitrag

- Problemframing als semantische Übersetzung,
- Trennung von Source, WIR und Target,
- Verlustledger und Reviewgrenze,
- Anti-Chore-Prinzip,
- Scope: kleine Spiele und Komponenten statt universeller AAA-Magie.

## Beweise

- [TRIVIUM README](https://github.com/Lootziffer666/TRIVIUM/blob/main/README.md) — meaning-not-syntax, WIR, drei Schichten, Exitcode 2, implementiert/geplant getrennt.

## Gegenhypothese

Das Universalitätsversprechen könnte konzeptionell größer sein als die aktuelle Implementation. Genau deshalb wird die Kompetenz auf **semantisches Compiler-/Übersetzungsdesign** begrenzt, nicht auf vollständige Engine-Interoperabilität.

## Evidenzstufe

**E3** für Architektur und Wahrheitsgrenzen.  
**E2** für breite reale Konversion.

## Legitimer Claim

> Designed a meaning-preserving game translation architecture with an intermediate world representation, explicit loss accounting, and human-review exits.

---

# Fallstudie 4 — SWIFT + SHADED

## Problem

3D-Modelle, Sprites und atmosphärische Szenen liegen gewöhnlich in getrennten Pipelines. Ihre Verbindung ist oft implizit, verlustreich und schwer reproduzierbar.

## Systementscheidung

SWIFT erzeugt deterministische Sprite-Artefakte und maschinenlesbare Manifeste. SHADED verwendet Actor-/Materialverträge, um diese Artefakte in eine shader-first Welt zu integrieren. Die sichtbare Welt soll selbst zur Wahrheitsschicht werden: Was dargestellt wird, muss mit Interaktion und Kollision übereinstimmen.

## Persönlicher Beitrag

- Pipelinegrenzen und Übergabeformate,
- Manifest als Wahrheitsträger,
- Actor-Konzept zwischen Sprite und Welt,
- visuelle Konsistenz als Systeminvariante,
- Environmental Storytelling als Laufzeitstruktur statt Dekoration.

## Beweise

- [SWIFT README](https://github.com/Lootziffer666/SWIFT/blob/main/README.md) — CLI, Manifeste, deterministische Pipeline, Exitcodes, SHADED-Integration.
- [SHADED README](https://github.com/Lootziffer666/SHADED/blob/main/README.md) — one-image world, Actor, Materialpalette, deterministische Marker-Korrektur.

## Evidenzstufe

**E3** für Pipeline- und Contract-Design.  
**E2/E3** für vollständige visuelle Produktionsqualität über große Assetmengen.

## Legitimer Claim

> Directed a contract-based 3D-to-sprite-to-world pipeline in which generated assets carry machine-readable provenance and visual state remains aligned with interaction state.

---

# Fallstudie 5 — MIXTRACT

## Problem

Audio-Werkzeuge behaupten schnell, Stimmen oder Instrumente „extrahiert“ zu haben, obwohl sie nur Spektren, Schätzungen oder Platzhalter liefern. Das erzeugt eine gefährliche Lücke zwischen UI-Claim und tatsächlichem Output.

## Systementscheidung

MIXTRACT trennt Roh-Audioanalyse von echter Stem-/Source-Extraktion. Das README markiert klar, was funktioniert und was defekt oder noch nicht implementiert ist. JSON-Summaries, Diagnostik und Outputpfade sollen maschinenlesbar und ehrlich sein.

## Persönlicher Beitrag

- Definition der Wahrheitsgrenze,
- Ablehnung von „fake success“,
- klare Status- und Ergebnissemantik,
- Produktanforderung, dass Diagnose und Output exakt sagen, was erzeugt wurde.

## Beweise

- [MIXTRACT README](https://github.com/Lootziffer666/MIXTRACT/blob/main/README.md) — Analyse vs Extraktion, Working/Broken-Status, exakte Outputs und Diagnostik.

## Evidenzstufe

**E4/E3** für Failure Honesty und Outputvertrag.  
**E2** für hochwertige Quellentrennung als fertige Funktion.

## Legitimer Claim

> Established explicit truth boundaries for an audio-analysis pipeline, preventing analytical estimates from being mislabeled as extracted source material.

---

# Fallstudie 6 — MYTHIC

## Problem

Zwischen „Repo funktioniert“ und „App ist erreichbar“ liegen Buildsysteme, Secrets, Domains, Proxy, TLS, Abhängigkeiten und fehlertolerante Provisionierung. Für Nichtentwickler ist diese letzte Meile besonders reibungsreich.

## Systementscheidung

MYTHIC ist ein self-hosted Deployment-Service für vibe-coded Apps. Es unterstützt mehrere Deployments, sortiert Abhängigkeiten topologisch, überspringt abhängige Deployments nach Fehlern und speichert BYOK-Konfiguration verschlüsselt. Der Scope ist ausdrücklich enger als eine universelle Cloudplattform.

## Persönlicher Beitrag

- One-click-Produktfluss,
- Own-repos-only-Scope,
- Fehler- und Abhängigkeitssemantik,
- OAuth-/Repo-Picker- und Domain-Anforderungen,
- klare Reifegrad- und Nicht-Ziel-Definition.

## Beweise

- [MYTHIC README](https://github.com/Lootziffer666/MYTHIC/blob/main/README.md) — Multideploy, Dependency Ordering, BYOK, Architektur, Reifegrad.

## Evidenzstufe

**E3** für Produkt- und Architekturdesign.  
**E2** für produktive Zuverlässigkeit auf heterogenen Repos.

## Legitimer Claim

> Designed a self-hosted deployment product that turns repository intent into ordered, failure-aware deployment jobs with encrypted BYOK configuration.

---

# Fallstudie 7 — LAUNCHPAD + KIDS_LAUNCHER + DESIGN_SYSTEM

## Problem

Kinderoberflächen sind häufig bloß vereinfachte Erwachsenensysteme. Werbung, Stores, versteckte Menüs, Touch-Zwang und unklare Zustände erzeugen Risiko und Friktion.

## Systementscheidung

LAUNCHPAD verfolgt eine kioskartige, touch-first Oberfläche mit kuratierten Apps, Elternmodus und klaren Grenzen. KIDS_LAUNCHER formuliert Controller-first, große Icons, wenig Text, keine externen Links, Stores oder Werbung sowie Eltern-PIN. DESIGN_SYSTEM trennt semantische Tokens von konkreten Farben und verankert Accessibility-Primitives.

## Persönlicher Beitrag

- Nutzerperspektive des Kindes statt technischer App-Liste,
- „Spielen, nicht suchen“ als Interaktionsprinzip,
- Eltern-Gate und sichere Defaults,
- semantische Design-Tokens,
- reduzierte kognitive Last.

## Beweise

- [LAUNCHPAD README](https://github.com/Lootziffer666/LAUNCHPAD/blob/main/README.md)
- [KIDS_LAUNCHER README](https://github.com/Lootziffer666/KIDS_LAUNCHER/blob/main/README.md)
- [DESIGN_SYSTEM README](https://github.com/Lootziffer666/DESIGN_SYSTEM/blob/main/README.md)

## Evidenzstufe

**E3** für UX- und Sicherheitsprinzipien.  
**E2** für empirisch validierte Kindertauglichkeit.

## Legitimer Claim

> Designed child-centered launcher interactions around controller/touch accessibility, safe defaults, parental gates, and reduced reading/navigation load.

---

# Fallstudie 8 — RAPIER

## Problem

Coding-Agenten sind zwar automatisiert, ihre Steuerung bindet den Nutzer dennoch an Tastatur, Desktop und Toolwechsel. Für mobile Arbeit und spontane Gedanken bleibt Reibung bestehen.

## Systementscheidung

RAPIER kombiniert Voice Capture mit Routing zu Claude/Codex und behandelt Sprache als Auftragsschicht. Das Ziel ist nicht bloß Diktat, sondern live geroutete Agentenarbeit mit passender Rolle und Kontext.

## Persönlicher Beitrag

- Voice-first Produktmodell,
- mobile Auftrag-/Entscheidungsschicht,
- Trennung von Nutzer, Werkbank, Arbeiter und Bauleiter,
- Routing statt einheitlichem Allzweckagenten.

## Beweise

- [RAPIER README](https://github.com/Lootziffer666/RAPIER/blob/main/README.md) — Voice Capture, Router, Chatmodell, Deployment.

## Evidenzstufe

**E2/E3**. Die Produktidee und Architektur sind klar; ein belastbarer Alltagstest und stabile End-to-End-Nutzung müssen noch dokumentiert werden.

## Legitimer Claim

> Prototyped a voice-first control layer that routes spoken development intent to specialized coding agents instead of forcing users into desktop-bound chat workflows.
