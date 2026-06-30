# 3m5 Skill Hub

Ein kuratierter **Claude Plugin Marketplace** für [Claude Code](https://code.claude.com) und **Claude Cowork**.

## Enthaltene Plugins

| Plugin | Beschreibung |
|--------|-------------|
| `3m5` | Enthält den `grill-me`-Skill: stellt hartnäckige Fragen zu einem Plan oder Design, bis ein gemeinsames Verständnis erreicht ist. |

## Enthaltene Skills (`3m5`-Plugin)

| Skill | Aufruf | Beschreibung |
|-------|--------|-------------|
| `grill-me` | `/3m5:grill-me` | Relentless interview – stellt hartnäckige Fragen zu einem Plan oder Design. |
| `happy-wife` | `/3m5:happy-wife` | Beantwortet alles als genervte, passiv-aggressive Ehefrau. Korrekte Antworten, verpackt in häusliche Bitterkeit. |

## Installation

### Claude Code

```bash
/plugin marketplace add https://gitlab.3m5.de/suchandt/3m5-skill-hub.git
/plugin install grill-me@3m5-skill-hub
```

### Claude Cowork

Denselben Git-Marketplace als Quelle hinzufügen und `grill-me` installieren —
das Format ist identisch, da der Skill vollständig self-contained ist (kein
Slash-Command erforderlich).

## Verwendung

Nach der Installation den Skill explizit aufrufen:

```
/3m5:grill-me
```

Oder in natürlicher Sprache: „Grill mich zu meinem Plan" / „Stell mir harte Fragen zu diesem Design".

## Erweiterung

Weitere Plugins nach demselben Muster ergänzen:

1. Verzeichnis `plugins/<plugin-name>/` anlegen
2. `plugins/<plugin-name>/.claude-plugin/plugin.json` erstellen
3. Skills unter `plugins/<plugin-name>/skills/<skill-name>/SKILL.md` ablegen
4. Plugin in `.claude-plugin/marketplace.json` unter `plugins[]` registrieren

## Lizenz

MIT
