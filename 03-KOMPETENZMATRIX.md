# 03 — Kompetenzmatrix

## Bewertungslogik

- **Belegstärke:** E0 bis E4 gemäß Methodik.
- **Konfidenz:** Wie sicher ist die Inferenz aus mehreren Quellen?
- **Beitragstyp:** H = menschliche semantische Autorschaft, A = Agentenimplementierung, J = gemeinsame Orchestrierungsleistung.
- **Nicht ableiten:** Schutz gegen überzogene CV-Claims.

## Matrix

| Kompetenz | Zentrale Evidenz | Stufe | Beitrag | Konfidenz | Nicht ableiten |
|---|---|---:|---|---|---|
| Problem- und Bedeutungsmodellierung | CATCHIT Live Truth vs Structural Contract; TRIVIUM meaning-not-syntax | E4/E3 | H/J | sehr hoch | wissenschaftliche Formalmethoden-Ausbildung |
| Zustandsmaschinen und Übergangslogik | CATCHIT 42 Zustände, Guard, Transitionen, Persistenz | E4 | H/J/A | sehr hoch | manuelle Implementierung jeder Transition |
| Contract-first Systemdesign | JSON-Schemas, Manifeste, Evidence Bundles, Exitcodes | E4/E3 | H/J | sehr hoch | formale Verifikation im mathematischen Sinn |
| Agentenorchestrierung | ANVIL, GAIME, ANVIL-CLIENT, PR-Schleifen | E4/E3 | H/J | sehr hoch | Führung menschlicher Engineering-Teams |
| Qualitäts- und Gate-Design | CUE-AGENT, CATCHIT GATES, Strict Mode | E4 | H/J/A | sehr hoch | Security-Audit- oder QA-Zertifizierung |
| Failure Honesty / Unsicherheitsmodellierung | MIXTRACT, TRIVIUM, CUE-AGENT, CATCHIT | E4/E3 | H/J | sehr hoch | Fehlerfreiheit |
| Cross-repo-Architektur | WIZARD → SWIFT → SHADED → CUE; ANVIL Control Plane | E3 | H/J | hoch | produktiv bewiesene Skalierung des Gesamtsystems |
| UX als Zustandsarchitektur | CATCHIT, LAUNCHPAD, KIDS_LAUNCHER | E4/E3 | H/J | sehr hoch | klassische User-Research-Praxis mit großen Stichproben |
| Accessibility-/Stress-orientiertes Design | CATCHIT Recovery, große/klare Launcher-Flows | E3 | H/J | hoch | formale WCAG-Konformität aller Produkte |
| Design-System-Denken | DESIGN_SYSTEM Tokens/DNA, ANVIL-CLIENT, Launcher | E3 | H/J/A | hoch | Visual-Design-Meisterschaft ohne visuelle Fallstudien |
| Developer Experience / Reibungsreduktion | MYTHIC, RAPIER, ANVIL-CLIENT, BELLOWS | E3 | H/J | hoch | gemessene Unternehmens-DevEx-Verbesserung |
| Self-hosting- und Deployment-Produktdenken | MYTHIC Multideploy, BYOK, Dependency Ordering | E3 | H/J/A | mittel-hoch | SRE-/DevOps-Betriebsreife |
| Daten- und Provider-Abstraktion | CATCHIT Provideradapter, BELLOWS Routing | E3/E4 | H/J/A | hoch | tiefe Backend-Implementierungskompetenz ohne Agenten |
| Pipeline- und Artefaktdesign | SWIFT Manifests, SHADED Actor, TRIVIUM WIR | E3 | H/J | hoch | vollständige Interoperabilität aller Engines |
| Technische Dokumentationsarchitektur | Specs, GATES, Integrationsdocs, Statusgrenzen | E4/E3 | H/J/A | sehr hoch | alleinige Autorschaft aller Markdown-Dateien |
| Review- und Korrekturführung | CATCHIT PRs, Defektaudits, Merge-Konfliktkorrektur | E4/E3 | J | hoch | klassische Peer-Review-Erfahrung in Teams |
| Strategische Scope-Kontrolle | explizite Nicht-Ziele in ANVIL, MYTHIC, MIXTRACT | E3 | H/J | sehr hoch | immer kleine oder realistische Projektumfänge |
| Produktökosystem-Komposition | wiederverwendete Rollen und Verträge über viele Repos | E3 | H/J | hoch | abgeschlossene Plattformreife |
| Experimentelles Prototyping | viele domänenübergreifende lauffähige/teilweise Systeme | E3 | H/J/A | sehr hoch | langfristige Wartung oder Marktvalidierung |
| Rekombinatives Innovationsdenken | Transfer von State/Gate/Evidence-Prinzipien zwischen Domänen | E3 | H | hoch | wissenschaftlich gemessene Kreativität |

## 1. Höchste Beweisdichte

### Meaning-first Architecture

**Beobachtung:** Mehrere Repos trennen explizit zwischen Daten, Bedeutung, Darstellung und Entscheidung. CATCHIT unterscheidet Live Truth und Structural Contract; TRIVIUM übersetzt eine World Intermediate Representation; SWIFT und SHADED übergeben manifestierte Artefakte; CUE-AGENT prüft Beweise statt Selbstbeschreibung.

**Alternative Erklärung:** Die Begriffe könnten von Agenten vorgeschlagen worden sein.

**Warum die Inferenz trotzdem stark ist:** Dasselbe Prinzip taucht in unabhängigen Domänen, über mehrere Monate, mit unterschiedlichen Technologien und konkreten Gate-/State-Artefakten wieder auf. Die Auswahl und Kanonisierung des Prinzips ist selbst eine menschliche Systemleistung.

### Governance für AI-generierte Systeme

**Beobachtung:** ANVIL ist bewusst kein monolithischer Generator; CUE-AGENT verlangt evidence-basierte Prüfbündel; CATCHIT besitzt harte Gates; PRs durchlaufen Review- und Korrekturschleifen.

**Alternative Erklärung:** Die Agenten könnten auch Governance-Dateien selbst erzeugt haben.

**Warum die Inferenz stark ist:** Das Portfolio zeigt nicht nur Dokumente, sondern eine wiederholte Entscheidung gegen ungeprüfte Claims, stille Fallbacks und monolithische Zuständigkeit. Diese konsistente Auswahl ist das relevante Signal.

## 2. Mittlere Beweisdichte

### Deployment- und Infrastrukturkompetenz

MYTHIC belegt ein solides Produkt- und Architekturverständnis für Deployment-Flows. Es belegt noch keine jahrelange Betriebsverantwortung, Incident Response oder SRE-Praxis. Der richtige Claim lautet:

> Entwirft und dirigiert self-hosted Deployment-Produkte und Provisioning-Flows.

Nicht:

> Erfahrener DevOps Engineer.

### Visual Design

DESIGN_SYSTEM, SHADED und Launcher-Projekte belegen Designsystem- und Atmosphärenintention. Ohne kuratierte Vorher/Nachher-Screenshots, Accessibility-Prüfungen und externe Nutzerbeobachtung bleibt die visuelle und empirische UX-Qualität nur teilweise belegt.

## 3. Kompetenzen, die ausdrücklich offen bleiben

- manuelle Programmiertiefe pro Sprache,
- klassische Algorithmik ohne AI-Hilfe,
- Teamführung und Konfliktmoderation,
- Kosten-, Umsatz- oder Markterfolg,
- Produktionsbetrieb unter Last,
- systematische User Research mit externen Testpersonen,
- Security Engineering und Penetration Testing,
- akademische Forschungskompetenz,
- langfristige Maintenance über mehrere Jahre.

## 4. Sprach- und Technologieinventar — korrekt gelesen

Die Repos enthalten unter anderem Kotlin, TypeScript, JavaScript, Python, Java, Dart, Go, HTML, CSS, WebGL/GLSL, Docker, Android, Next.js, Blender und SQLite.

Das belegt:

- Fähigkeit, heterogene Implementationsräume über Agenten zu koordinieren,
- Fähigkeit, Technologiegrenzen und Übergabeverträge zu definieren,
- Erfahrung mit den Konsequenzen verschiedener Plattformen.

Es belegt **nicht automatisch**:

- unabhängige Syntaxbeherrschung,
- Debugging ohne Agenten,
- Interviewfähigkeit zu Sprachinternas,
- Produktionsseniorität in jedem Stack.

Die richtige Portfolio-Rubrik heißt deshalb nicht „Programmiersprachen“, sondern:

> **Implementation environments directed through AI-assisted workflows**
