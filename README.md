# coptic-claude-plugin

Plugin Claude Code (et sa marketplace) qui regroupe les agents partagés par les applications coptes orthodoxes d'ASEL : KatamerosCopte, LivreAGPIA, coptic-calendar-core et les futures applications d'offices.

## Agents
| Agent | Quand l'utiliser |
|---|---|
| `coptic-dev:coptic-calendar-expert` | Conversion des dates coptes, Pâques copte, fêtes et jeûnes mobiles, tests de la bibliothèque |
| `coptic-dev:lectionary-data-engineer` | Import du Katameros et du Synaxaire, schéma JSON, validation, manifest |
| `coptic-dev:android-app-dev` | Écrans Kotlin et Material 3, multilingue FR/AR/EN, build |
| `coptic-dev:android-widget-dev` | Widget d'écran d'accueil, mise à jour à minuit, Doze, tests sur émulateur |
| `coptic-dev:integration-architect` | Deep links `copte://`, ContentProvider partagé, JitPack, compatibilité |

Les skills de traduction et de terminologie (`glossaire-copte-orthodoxe`, `sources-citations-coptes`) restent dans ton espace claude.ai. Les agents y font référence.

## Installation
Dans Claude Code :
```text
/plugin marketplace add asel-hue/coptic-claude-plugin
/plugin install coptic-dev@coptic-tools
```
Les dépôts KatamerosCopte et coptic-calendar-core déclarent déjà cette marketplace dans `.claude/settings.json`. Une fois le dossier approuvé, il reste à lancer `/plugin install coptic-dev@coptic-tools` une fois par clone.

## Ajouter un agent
Crée `agents/<nom>.md`, avec le frontmatter `name`, `description` et `tools`, puis committe. Sans champ `version` dans `plugin.json`, les mises à jour suivent les commits.

## Licence
PolyForm Noncommercial 1.0.0, voir `LICENSE`.
