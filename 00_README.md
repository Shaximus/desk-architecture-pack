# Desk Architecture Pack

Paper-first architecture for a multi-agent trading *research* desk.
Not a live bot. Not financial advice. Not a copy of any viral X video.

## Why this exists

A cluster of September 2026 X posts sold the same costume:

- 6 or 8 or 200 "Grok Bots" as a trading floor
- overnight P&L with no public blotter
- a neon dashboard video
- sometimes a `t.co` bot-builder signup

The product underneath (Grok Bot) is real. The 5-minute Polymarket Up/Down market is real. A few public grind wallets are real. The claim that *you* can paste job titles into Grok Bot and print $418/day from $200 is not validated.

This repo keeps the parts that survive contact with official docs and market microstructure, and throws away the costume.

## Hard rules

1. No private keys in any agent context.
2. Exactly one execution writer, and it is deterministic code, not an LLM.
3. Human approval by ticket ID before any live send.
4. Ontario residents: do not use this pack to reach geo-blocked Polymarket. See `07_ontario_and_safety.md`.
5. Treat every strategy score as a pre-simulation estimate of *process quality*, not a promised return.

## File tree

| File | What it is |
|---|---|
| `01_credibility_audit.md` | The four viral posts, wallets, farm pattern |
| `02_sources.md` | Official docs, repos, papers |
| `03_architecture.md` | Planes, graph, N*, runtimes |
| `04_agent_cards/` | Role charters |
| `05_sim_spec.py` | Local paper simulator |
| `06_strategy_scores.md` | 1-100 scorecard |
| `07_ontario_and_safety.md` | Legal + shared-computer rules |
| `08_diminishing_returns.md` | N vs value |

## Fast start

```bash
python 05_sim_spec.py
```

Requires Python 3.10+ and numpy.

Then create at most six research seats from `04_agent_cards/`.
Do not create two hundred decision agents.
