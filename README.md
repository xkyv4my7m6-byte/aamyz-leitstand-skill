# AAMYZ Leitstand Skill

**Make AI-agent work visible while it is happening.** This small, model-agnostic skill teaches a coding agent to report when it starts, what changed, when it is waiting or blocked, and what evidence proves completion.

[Install the skill](https://github.com/xkyv4my7m6-byte/aamyz-leitstand-skill/releases/latest) · [Watch the 32-second demo](https://github.com/xkyv4my7m6-byte/aamyz-leitstand-skill/releases/latest) · [Report an issue](https://github.com/xkyv4my7m6-byte/aamyz-leitstand-skill/issues)

## What problem does it solve?

An AI agent can spend minutes running commands or changing files while the person using it sees no useful status. It may also say “done” without showing what proves that. The Leitstand Skill gives the agent a simple reporting rhythm:

1. Say what result it is working toward.
2. Share short updates when the work reaches a meaningful stage.
3. Say what it is waiting for or what is blocking it.
4. Mark work complete only with observable evidence.
5. Close the status entry when the session ends.

The goal is a clearer hand-off between a person and an AI agent. The skill does not claim to make an agent more capable or guarantee that its work is correct.

## What is included

- `skills/aamyz-leitstand/SKILL.md`: portable workflow instructions for an AI coding agent.
- This guide: what it does, how to install it, and how to measure GitHub interest.
- A small promotional video in the first GitHub Release.

## What is not included

This download is **not** AAMYZ OS and does **not** contain AAMYZ KI, an AI model, a dashboard, a status API, credentials, or a hosted service. The skill uses a status reporter only when your computer or project already provides one. Without one, it keeps progress visible in the conversation and tells you that no separate dashboard is connected. It sends no usage telemetry.

Choose and configure your own AI model and agent. The skill is instructions, not a model subscription.

## Install with GitHub CLI

Install [GitHub CLI](https://cli.github.com/) if it is not already installed, then run one command for the agent you use.

### Codex, all your projects

```powershell
gh skill install xkyv4my7m6-byte/aamyz-leitstand-skill skills/aamyz-leitstand --agent codex --scope user
```

### Claude Code, all your projects

```powershell
gh skill install xkyv4my7m6-byte/aamyz-leitstand-skill skills/aamyz-leitstand --agent claude-code --scope user
```

### Kimi Code CLI, all your projects

```powershell
gh skill install xkyv4my7m6-byte/aamyz-leitstand-skill skills/aamyz-leitstand --agent kimi-cli --scope user
```

To install only for the current project, replace `--scope user` with `--scope project`. Start a new agent session after installation so it can discover the skill. The install command supports other coding agents too; run `gh skill install --help` to see the current list.

### Install a fixed version

Use `skills/aamyz-leitstand@v0.1.0` in place of `skills/aamyz-leitstand` to pin the first release. To update later, use `gh skill update`.

### Manual installation

Download the ZIP from [Releases](https://github.com/xkyv4my7m6-byte/aamyz-leitstand-skill/releases), then copy the `skills/aamyz-leitstand` folder into the skill directory documented by your agent. For example, project-scoped installs commonly use `.agents/skills/` for Codex and `.claude/skills/` for Claude Code. Restart or open a new session afterward.

## Use it

After installation, ask your coding agent to use the AAMYZ Leitstand Skill for the task. For example:

> Use the AAMYZ Leitstand Skill. Tell me when you start, keep me updated at important stages, and show evidence when you say the work is finished.

The skill follows the project's own status-board instructions. It does not assume that every user has the AAMYZ local dashboard.

## Check whether people download it

GitHub shows different signals for different actions:

- **Release asset download count:** the number shown beside each attached file under the release. We will publish the install ZIP and demo video as separate assets, so their counts stay distinguishable.
- **Repository traffic:** open the repository's **Insights → Traffic** page. It shows visitors, page views, referring sites, popular content, and full Git clones for the last 14 days. A clone is not the same as a ZIP download, and the figures do not prove that someone installed or used the skill.
- **Stars, forks, and issues:** visible signs of interest and feedback, not download counts.

GitHub does not tell us who downloaded the files or whether the skill was installed. The skill has no tracking code. Review the numbers weekly during the first month and record the date and counts; compare the skill ZIP with the video asset to see which one attracted downloads.

## Feedback

Use [GitHub Issues](https://github.com/xkyv4my7m6-byte/aamyz-leitstand-skill/issues) to report unclear instructions, an unsupported agent, or a concrete example where the status flow helped or failed. Do not post secrets, private logs, or customer data.

## License

MIT. See [`LICENSE`](LICENSE).

---

# Deutsche Anleitung

**KI-Agenten bei der Arbeit sehen, statt auf eine stille Blackbox zu warten.** Der Skill bringt einem Coding-Agenten einen einfachen Statusablauf bei: Start, wichtige Zwischenstände, Warten oder Blockade und ein Abschluss mit überprüfbarem Beleg.

[Skill herunterladen](https://github.com/xkyv4my7m6-byte/aamyz-leitstand-skill/releases/latest) · [32-Sekunden-Demo ansehen](https://github.com/xkyv4my7m6-byte/aamyz-leitstand-skill/releases/latest) · [Fehler oder Feedback melden](https://github.com/xkyv4my7m6-byte/aamyz-leitstand-skill/issues)

## Was macht der Skill?

Eine KI kann länger an Dateien, Befehlen oder einem Build arbeiten, ohne dass der Nutzer einen brauchbaren Zwischenstand sieht. Manchmal meldet sie „fertig“, obwohl kein überprüfbarer Nachweis vorliegt. Der Leitstand-Skill gibt ihr einen klaren Ablauf:

1. Sie sagt, welches Ergebnis sie erreichen soll.
2. Sie meldet wichtige Fortschritte kurz und sachlich.
3. Sie sagt, worauf sie wartet oder was sie blockiert.
4. Sie meldet „fertig“ nur mit einem sichtbaren Beleg, zum Beispiel einem Testergebnis, einer Datei, einer Prüfsumme oder einer bestätigten Antwort.
5. Sie schließt den Status am Ende der Sitzung.

Der Skill macht den Ablauf nachvollziehbarer. Er macht eine KI nicht automatisch leistungsfähiger und garantiert nicht, dass deren Ergebnis richtig ist.

## Was ist enthalten?

- `skills/aamyz-leitstand/SKILL.md`: wiederverwendbare Anweisungen für einen KI-Coding-Agenten.
- Diese Anleitung mit Installation und Hinweisen zur Messung des Interesses.
- Ein kurzes Vorstellvideo als eigene Datei im ersten GitHub-Release.

## Was ist nicht enthalten?

Der Download enthält **weder AAMYZ OS noch AAMYZ KI**, kein KI-Modell, kein Dashboard, keine Status-Schnittstelle, keine Zugangsdaten und keinen gehosteten Dienst. Ein separates Dashboard funktioniert nur, wenn auf deinem Computer oder in deinem Projekt bereits ein passender Statusmelder eingerichtet ist. Ohne diesen meldet der Agent den Fortschritt im Chat und weist darauf hin, dass kein externes Statusboard verbunden ist. Der Skill sendet keine Nutzungsdaten.

Du wählst und konfigurierst dein eigenes KI-Modell und deinen Agenten. Der Skill ist eine Anleitung, kein Modell-Abo.

## Installation

Am einfachsten geht es mit der [GitHub CLI](https://cli.github.com/). Installiere sie, falls sie noch fehlt, und führe einen passenden Befehl aus.

**Codex, für alle Projekte:**

```powershell
gh skill install xkyv4my7m6-byte/aamyz-leitstand-skill skills/aamyz-leitstand --agent codex --scope user
```

**Claude Code, für alle Projekte:**

```powershell
gh skill install xkyv4my7m6-byte/aamyz-leitstand-skill skills/aamyz-leitstand --agent claude-code --scope user
```

**Kimi Code CLI, für alle Projekte:**

```powershell
gh skill install xkyv4my7m6-byte/aamyz-leitstand-skill skills/aamyz-leitstand --agent kimi-cli --scope user
```

Nur für das aktuelle Projekt ersetzt du `--scope user` durch `--scope project`. Öffne anschließend eine neue Agent-Sitzung, damit der Skill erkannt wird. Die GitHub CLI unterstützt weitere Coding-Agenten. Die aktuelle Liste zeigt `gh skill install --help`.

**Fest auf Version 0.1.0:** Ersetze `skills/aamyz-leitstand` durch `skills/aamyz-leitstand@v0.1.0`. Für spätere Aktualisierungen verwende `gh skill update`.

**Ohne GitHub CLI:** Lade die ZIP-Datei von [Releases](https://github.com/xkyv4my7m6-byte/aamyz-leitstand-skill/releases) herunter und kopiere den Ordner `skills/aamyz-leitstand` in den Skill-Ordner deines Agenten. Häufige Projektordner sind `.agents/skills/` für Codex und `.claude/skills/` für Claude Code. Danach eine neue Agent-Sitzung öffnen.

## Beispiel für die erste Nutzung

> Verwende den AAMYZ Leitstand-Skill. Sag mir, wann du beginnst, gib bei wichtigen Arbeitsschritten kurze Zwischenstände und belege mit einem Ergebnis, wenn du fertig bist.

Der Skill folgt den Statusboard-Regeln des jeweiligen Projekts. Er setzt nicht voraus, dass jeder Nutzer das AAMYZ-Leitstand-Dashboard hat.

## Downloads und Interesse messen

- **Downloadzahl einer Release-Datei:** Unter dem Release zeigt GitHub die Zahl je Datei. Das Skill-Paket und das Vorstellvideo werden als getrennte Dateien angehängt, damit ihre Downloadzahlen unterscheidbar sind.
- **Aufrufe und Klone:** Im Repository unter **Insights → Traffic** zeigt GitHub Besucher, Seitenaufrufe, Verweisquellen, beliebte Inhalte und vollständige Klone der letzten 14 Tage. Ein Klon ist kein ZIP-Download. Die Zahlen beweisen nicht, dass jemand den Skill installiert oder verwendet hat.
- **Sterne, Forks und Issues:** sichtbares Interesse und Rückmeldungen, aber keine Downloadzahlen.

GitHub zeigt nicht, wer etwas heruntergeladen hat oder ob eine Installation erfolgreich war. Der Skill enthält keine Nachverfolgung. Notiere die Zahlen im ersten Monat einmal pro Woche und vergleiche die Downloads des Skill-Pakets mit denen des Videos.

## Lizenz

MIT. Einzelheiten stehen in [`LICENSE`](LICENSE).
