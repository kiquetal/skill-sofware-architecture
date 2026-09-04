# Software Architecture — Learning Notes

Learning notes and findings from the O'Reilly skill: **Software Architecture**
Source: https://learning.oreilly.com/skill/software-architecture/0642572295189/

Started: 2026-08-28

This repo tracks my progress through all **5 levels / 43 competencies** of the skill.
Each level has its own file under [`levels/`](./levels); cross-cutting synthesis notes
live under [`concepts/`](./concepts) as I create them.

---

## Progress Dashboard

| Level | Name | Competencies | Done | Status | Notes |
|-------|------|:------------:|:----:|--------|-------|
| [1](./levels/level-1-exploring.md) | Exploring | 15 | 15/15 | 🟢 Verified | Architecture thinking, styles, characteristics, data |
| [2](./levels/level-2-applying.md) | Applying | 12 | 5/12 | 🟡 In progress | Designing, component identification, coupling |
| 3 | Building | tbd | — | ⚪ Not started | |
| 4 | Advancing | tbd | — | ⚪ Not started | |
| 5 | Expert | tbd | — | ⚪ Not started | |

**Overall:** 15 / 43 competencies verified _(15 mapped for Level 1; Levels 2–5 counts pending)_.

Status legend: 🟢 Done · 🟡 In progress · 🔴 Known gap · ⚪ Not started

---

## Repository Layout

```
.
├── README.md                    # This index / progress dashboard
├── levels/
│   └── level-1-exploring.md     # Level 1 — 15 competencies
├── concepts/                    # Cross-cutting synthesis notes (added lazily)
└── diagrams/                    # Practice diagrams (C4 / UML / mermaid)
```

---

## How I use these notes

- One file per **level**; one section per **competency** inside it.
- For each competency: capture the **concept**, an explanation **in my own words**, and a **key takeaway**.
- Use [`concepts/`](./concepts) for synthesis that spans competencies (e.g., an architecture-styles comparison table) — this is where the real learning consolidates.
- Update this dashboard's Done/Status columns as I complete competencies.

---

## References

- O'Reilly Skill: Software Architecture — https://learning.oreilly.com/skill/software-architecture/0642572295189/
- _Fundamentals of Software Architecture_ — Mark Richards & Neal Ford
- _Software Architecture: The Hard Parts_ — Neal Ford, Mark Richards, et al.
