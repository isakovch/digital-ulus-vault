# Digital ULUS — Vault

This is the knowledge vault of Khan, managed by six Telegram bots and read via Obsidian.

## Structure

- `00-Inbox/` — raw messages, not yet classified
- `10-Knowledge/` — mature entities
  - `Exchange/` — TCX, торговая платформа, FX продукты
  - `Invest/` — White Label, securities, NYSE/NASDAQ
  - `Pay/` — Kagan Pay, карты, BIN sponsors
  - `Strategy/` — стратегия, конкуренты, гипотезы
- `20-People/` — партнёры, контакты, контрагенты
- `30-Sources/` — saved links and summaries
- `90-System/` — system logs (agent actions, conflicts)
- `.ulus/` — hidden technical files (sqlite databases)

## File format

Every entity is a markdown file with YAML frontmatter:

```markdown
---
id: 20260512-rox-erc3643
type: Idea
sub_category: Strategy
status: Active
created: 2026-05-12T14:30:00+06:00
related:
  - "[[20260415-rox-valuation]]"
tags: [tokenization, rox-deal]
---

# Title

Body in markdown...
```

## Obsidian setup

1. Open Obsidian, "Open folder as vault" → select this directory
2. Install plugin "Obsidian Git" → enable auto-pull every 1-2 minutes
3. Recommended plugins: "Graph view" (built-in), "Dataview" (for queries)

## Read-only convention

This vault is primarily written by bots. Khan can read freely; manual edits
should be made in Obsidian, then `git push` from Mac so the VPS picks up
changes via its scheduled `git pull`.
