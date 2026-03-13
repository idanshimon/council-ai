# 🏛️ council-ai

AI-assisted city council workspace for Oregon municipalities. Built with [OpenClaw](https://github.com/openclaw/openclaw).

## What Is This?

A ready-to-use workspace that helps city councilors make better decisions on ordinances by checking them against state and federal law — automatically.

Built for **West Linn, Oregon** but adaptable to any Oregon city.

## What's Inside

```
├── SOUL.md                          # AI persona — legal advisor + meeting manager
├── USER.md                          # City-specific profile (West Linn)
├── AGENTS.md                        # Workflows for meetings & ordinance analysis
├── TOOLS.md                         # Local URLs, contacts, resources
├── MEMORY.md                        # Long-term institutional memory
├── meetings/
│   ├── agendas/                     # Drop agendas here before meetings
│   ├── minutes/                     # Post-meeting summaries
│   ├── prep/                        # Auto-generated briefing packets
│   └── action-items.md              # Running action item tracker
├── ordinances/
│   ├── drafts/                      # Working ordinance drafts
│   ├── analysis/                    # Legal consistency analyses
│   └── pipeline.md                  # Ordinance tracking (proposal → adoption)
└── reference/
    ├── oregon-revised-statutes.md   # Comprehensive ORS index (~14KB)
    ├── preemption-notes.md          # 🔴🟡🟢 what you can/can't legislate
    ├── federal-frameworks.md        # Constitutional limits & key cases
    ├── metro-regional.md            # Metro Functional Plan compliance
    └── west-linn-municipal-code.md  # Municipal code reference
```

## How It Works

1. **Drop an agenda** into `meetings/agendas/` and ask for a briefing
2. **Propose an ordinance** — the AI checks preemption (state & federal), finds comparable city examples, and drafts with proper legal framing
3. **After a meeting** — paste notes and get structured minutes, action items, and vote tracking
4. **Over time** — institutional memory builds in `MEMORY.md`, capturing decisions, legal interpretations, and policy positions

### Preemption Check (the key feature)

Every ordinance analysis starts with the traffic-light system in `preemption-notes.md`:

- 🔴 **Full preemption** — Can't legislate (firearms, minimum wage, rent control)
- 🟡 **Partial preemption** — Limited authority (land use, cannabis, housing)
- 🟢 **Local authority** — Go for it (noise, nuisance, traffic, utilities)

## Example: Electric Leaf Blower Ordinance

See [`ordinances/drafts/electric-leaf-blower-ordinance.md`](ordinances/drafts/electric-leaf-blower-ordinance.md) — a complete draft ordinance requiring electric-only leaf blowers by 2028, including:

- Proper legal framing (use regulation, not emissions — avoids federal CAA preemption)
- Owner liability (Portland enforcement model)
- Graduated penalties with appeals process
- Hardship waivers for commercial operators
- Internal legal analysis notes

## Setup

1. Install [OpenClaw](https://docs.openclaw.ai)
2. Clone this repo into your OpenClaw workspace
3. Fill in the `[brackets]` in `USER.md` and `TOOLS.md` with your city's details
4. Start chatting — ask about an ordinance topic and watch it work

## Adapting for Other Oregon Cities

1. Update `USER.md` with your city's info (population, council structure, contacts)
2. Update `TOOLS.md` with your municipal code URL and meeting details
3. Check `reference/preemption-notes.md` — preemption rules are statewide, but population triggers differ:
   - Cities >25,000: HB 2001 middle housing applies
   - Cities >10,000: Some additional housing requirements
   - Portland metro vs. standard vs. nonurban: minimum wage tiers differ
4. Update `reference/metro-regional.md` if you're outside Metro's boundary (or delete it)
5. Update `reference/west-linn-municipal-code.md` with your own municipal code

## ⚠️ Disclaimer

This is a **research assistance tool**, not legal advice. Always consult your city attorney before introducing or adopting any ordinance. AI can miss things, laws change, and your specific situation matters.

## License

MIT — use it, fork it, adapt it for your city.
