# 10 — Evidenzregister

## Zweck

Dieses Register verbindet zentrale Claims mit konkreten Artefakten. Es ist kein vollständiges Repo-Inventar, sondern eine Prüfliste für die wichtigsten Portfolioaussagen.

| ID | Claim | Primärartefakt | Stufe | Einschränkung |
|---|---|---|---:|---|
| E-001 | Modelliert komplexes Verhalten als kanonische Zustandsmaschine | [CATCHIT State Machine Spec](https://github.com/Lootziffer666/CATCHIT/blob/main/docs/CATCHIT_STATE_MACHINE_SPEC_v1.md) | E4 | Repo privat; öffentliche Evidence-Kopie nötig |
| E-002 | Trennt Live-Datenwahrheit von struktureller Wahrheit | [CATCHIT README](https://github.com/Lootziffer666/CATCHIT/blob/main/README.md) | E4/E3 | reale Feldwirksamkeit nicht gemessen |
| E-003 | Verwendet harte Akzeptanz- und Screenshot-Gates | [CATCHIT GATES](https://github.com/Lootziffer666/CATCHIT/blob/main/GATES.md) | E4 | Gate-Ausführung pro Release separat belegen |
| E-004 | Entwirft Control Plane statt monolithischem Generator | [ANVIL README](https://github.com/Lootziffer666/ANVIL/blob/main/README.md) | E3 | End-to-End aller Engines nicht vollständig öffentlich reproduziert |
| E-005 | Akzeptiert Beweise statt Agentenclaims | [CUE-AGENT README](https://github.com/Lootziffer666/CUE-AGENT/blob/main/README.md) | E4/E3 | tatsächliche Coverage der Checks prüfen |
| E-006 | Übersetzt Spielbedeutung über Zwischenrepräsentation | [TRIVIUM README](https://github.com/Lootziffer666/TRIVIUM/blob/main/README.md) | E3 | Universalität nicht belegt |
| E-007 | Modelliert unsichere Konversion als Human Review | [TRIVIUM README](https://github.com/Lootziffer666/TRIVIUM/blob/main/README.md) | E3 | konkrete Konversionsfälle als Demo ergänzen |
| E-008 | Erzeugt deterministische Sprite-Artefakte mit Manifest | [SWIFT README](https://github.com/Lootziffer666/SWIFT/blob/main/README.md) | E3 | Qualitäts-/Performancevergleich fehlt |
| E-009 | Verknüpft visuelle Welt und Actor-Vertrag | [SHADED README](https://github.com/Lootziffer666/SHADED/blob/main/README.md) | E3 | skalierte Szenen-/Kollisionstests fehlen |
| E-010 | Trennt Analyse von echter Audioextraktion | [MIXTRACT README](https://github.com/Lootziffer666/MIXTRACT/blob/main/README.md) | E4/E3 | Extraktionsqualität selbst nur teilweise belegt |
| E-011 | Entwirft failure-aware Self-hosted Deployment | [MYTHIC README](https://github.com/Lootziffer666/MYTHIC/blob/main/README.md) | E3 | Produktionsbetrieb unter Last nicht belegt |
| E-012 | Kapselt Provider, Budget und Routing | [ANVIL-BELLOWS README](https://github.com/Lootziffer666/ANVIL-BELLOWS/blob/main/README.md) | E3 | tatsächliche Providerabdeckung verifizieren |
| E-013 | Entwirft Operator-Cockpit mit Audit/BYOK | [ANVIL-CLIENT README](https://github.com/Lootziffer666/ANVIL-CLIENT/blob/main/README.md) | E3/E2 | Nutzerfluss als Video/Screenshot ergänzen |
| E-014 | Entwickelt controller-first Kindersicherheit | [KIDS_LAUNCHER README](https://github.com/Lootziffer666/KIDS_LAUNCHER/blob/main/README.md) | E3/E2 | Setup-Status; Usability nicht empirisch geprüft |
| E-015 | Entwickelt kiosk-/touch-first Launcher-UX | [LAUNCHPAD README](https://github.com/Lootziffer666/LAUNCHPAD/blob/main/README.md) | E3 | private/visuelle Evidence nötig |
| E-016 | Verwendet semantische Design-Tokens | [DESIGN_SYSTEM README](https://github.com/Lootziffer666/DESIGN_SYSTEM/blob/main/README.md) | E3 | visuelle Komponentenprüfung ergänzen |
| E-017 | Entwirft voice-first Agentenrouting | [RAPIER README](https://github.com/Lootziffer666/RAPIER/blob/main/README.md) | E2/E3 | stabiler Alltagstest fehlt |
| E-018 | Orchestriert Agenten über Rollen in Game-Build-Pipeline | [GAIME README](https://github.com/Lootziffer666/GAIME/blob/main/README.md) | E3/E2 | Umfang realer autonomer Runs prüfen |
| E-019 | Führt kanonische Konsistenzaudits durch | [CATCHIT PR #70](https://github.com/Lootziffer666/CATCHIT/pull/70) | E4/E3 | Reviewer teils automatisiert |
| E-020 | Iteriert State-/Surface-Architektur über PRs | [PR #77](https://github.com/Lootziffer666/CATCHIT/pull/77), [#78](https://github.com/Lootziffer666/CATCHIT/pull/78), [#79](https://github.com/Lootziffer666/CATCHIT/pull/79) | E4/E3 | Merge allein beweist keine Feldqualität |

## Beweisfamilien

### A. Canonical truth

- CATCHIT Decision Lock
- CATCHIT State Machine
- TRIVIUM WIR
- MIXTRACT Output Truth

### B. Agent governance

- ANVIL Control Plane
- CUE-AGENT Evidence Gate
- ANVIL-CLIENT Audit Surface
- ANVIL-BELLOWS Provider/Budget Guard

### C. Artifact pipelines

- SWIFT Manifest
- SHADED Actor/Material Contract
- TRIVIUM Loss Ledger

### D. Frictionless UX

- CATCHIT One-space Surface
- LAUNCHPAD kiosk model
- KIDS_LAUNCHER controller-first model
- MYTHIC one-flow deployment
- RAPIER voice capture/router

### E. Process proof

- CATCHIT PR history
- GATES.md
- strict modes and exitcodes
- machine-readable summaries
- screenshots and evidence directories

## Claim-Formulierungsregel

### Stark

> Defined and directed …  
> Designed the contract/state model for …  
> Orchestrated implementation and validation of …  
> Established evidence gates for …

### Nur bei manueller Einzelevidenz

> Implemented from scratch …  
> Expert in [language] …  
> Built the entire codebase independently …

## Noch zu exportierende öffentliche Evidence

1. Redigierte CATCHIT-State-Machine-Auszüge.
2. Ein vollständiges CUE-AGENT Evidence Bundle.
3. Ein SWIFT→SHADED End-to-End-Run mit Manifest und Screenshots.
4. Ein TRIVIUM Vorher/WIR/Nachher-Beispiel inklusive Loss Ledger.
5. Ein MYTHIC Deployment-Run mit Fehlerfall.
6. Ein MIXTRACT Beispiel, das Analyse und Extraktion sichtbar unterscheidet.
7. Ein kurzes Video des agentischen Arbeitskreislaufs von Auftrag bis Evidence.
