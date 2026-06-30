<p align="center">
  <img src="docs/banner.svg" alt="3m5. Webengineers — Plugin Hub" width="100%">
</p>

<p align="center">
  <a href="https://github.com/3m5/plugin-hub/blob/main/LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License: MIT"></a>
  <a href="https://github.com/3m5/plugin-hub/commits/main"><img src="https://img.shields.io/github/last-commit/3m5/plugin-hub" alt="Last commit"></a>
  <a href="https://github.com/3m5/plugin-hub/pulls"><img src="https://img.shields.io/github/issues-pr/3m5/plugin-hub" alt="Open PRs"></a>
  <img src="https://img.shields.io/badge/Claude-Code%20%7C%20Cowork-034185?logo=anthropic&logoColor=white" alt="Claude Code & Cowork">
</p>

# 3m5 Plugin Hub

> Kuratierte **Claude-Plugins** für alle 3m5-Abteilungen — nutzbar in **Claude Code** und **Claude Cowork**.

Ein Skill ist ein vordefiniertes Verhalten für Claude. Sie rufen ihn per Slash-Command auf, und
Claude verhält sich sofort genau so, wie der Skill es beschreibt — ohne langes Konfigurieren.

Die Skills sind nach **Abteilungen** organisiert. Jede Abteilung ist ein eigenes Plugin. Sie
installieren das Plugin Ihrer Abteilung plus `shared` — und erhalten genau die Skills, die zu
Ihrer Arbeit passen.

---

## 01. Die Abteilungen

### `shared` — für alle
Rollenübergreifende Skills, die in jeder Abteilung nützlich sind. Dieses Plugin sollten Sie
immer installieren.
*Beispiel: `happy-wife`.*

### `projektmanagement`
Skills rund um Planung und Anforderungen: einen Plan oder ein Design auf Herz und Nieren prüfen,
Kundenwünsche in saubere User Stories überführen, Anforderungen schärfen.
*Beispiele: `grill-me`, `storytelling`.*

### `design`
Skills für die Design-Arbeit: UI/UX-Feedback, Figma-Workflows und Design-Dokumentation.
*(Skills in Entwicklung.)*

### `development`
Skills für die Entwicklung: Code-Review, Refactoring, Security-Checks und technische
Dokumentation.
*(Skills in Entwicklung.)*

### `backoffice`
Skills für das Backoffice: E-Mail-Kommunikation, Dokumentenverarbeitung und Vorlagen.
*(Skills in Entwicklung.)*

> Eine vollständige Liste der enthaltenen Skills finden Sie jeweils in der README des Plugins
> unter `plugins/<abteilung>/`.

---

## 02. Installation

### Claude Code

> **Einmalig zuerst:** Den Marketplace als Quelle hinzufügen.
> ```
> /plugin marketplace add https://github.com/3m5/plugin-hub.git
> ```

Dann `shared` plus das Plugin Ihrer Abteilung installieren:

```
/plugin install shared@plugin-hub
/plugin install projektmanagement@plugin-hub
```

Verfügbare Plugins: `shared`, `projektmanagement`, `design`, `development`, `backoffice`.

### Claude Cowork — persönlich

1. Öffnen Sie den **Cowork**-Tab
2. Klicken Sie oben rechts auf **Customize**
3. Wechseln Sie zur Registerkarte **Plugins**
4. Klicken Sie in der Sektion „Personal plugins" auf **+**
5. Wählen Sie **Add marketplace → Add from a repository**
6. Geben Sie die Repository-URL ein:
   ```
   https://github.com/3m5/plugin-hub.git
   ```
7. Nach der Synchronisierung erscheinen alle Plugins unter „Browse plugins" —
   wählen Sie das Plugin Ihrer Abteilung und klicken Sie **Install**

### Claude Cowork — organisationsweit (Admin)

1. Öffnen Sie **Organization settings → Plugins**
2. Klicken Sie auf **Add marketplace** und wählen Sie **GitHub** als Quelle
3. Geben Sie das Repository im Format `owner/repo` ein: `3m5/plugin-hub`
4. Aktivieren Sie optional **Sync automatically**, damit Aktualisierungen
   automatisch übernommen werden
5. Die Plugins stehen anschließend allen Mitgliedern der Organisation zur Verfügung

---

## 03. Verwendung

Nach der Installation einfach den Skill-Namen eingeben (Schema `/<abteilung>:<skill>`):

```
/projektmanagement:grill-me
```

Claude erkennt einen Skill auch in natürlicher Sprache, etwa „Grill mich zu meinem Plan".

---

## 04. Beitragen

Skills liegen als einzelne Markdown-Dateien im Repository. Einen neuen Skill hinzufügen:

1. `SKILL.md` unter `plugins/<abteilung>/skills/<skill-name>/SKILL.md` anlegen
2. Den Skill in der README des jeweiligen Plugins ergänzen

Neue Abteilung (= neues Plugin) anlegen:

1. Verzeichnis `plugins/<abteilung>/` anlegen
2. `plugins/<abteilung>/.claude-plugin/plugin.json` erstellen
3. Skills unter `plugins/<abteilung>/skills/<skill-name>/SKILL.md` ablegen
4. Plugin in `.claude-plugin/marketplace.json` unter `plugins[]` registrieren
5. Die Abteilung oben in dieser README beschreiben

---

<p align="center">
  <sub><b>3m5. Media GmbH</b> — Webengineers · Dresden · München · Stuttgart · Frankfurt · Hamburg</sub><br>
  <sub>Lizenz: MIT</sub>
</p>
