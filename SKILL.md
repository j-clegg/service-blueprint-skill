# Service Blueprint Skill

Generate professional service blueprints following established methodology from Nielsen Norman Group, UK Government Digital Service, and Practical Service Design.

## Quick Start

1. **Read METHODOLOGY.md** — How to think about and facilitate blueprinting
2. **Define data using SCHEMA.md** — Structured JSON format for blueprint content
3. **Render using RENDERING.md** — HTML or Mermaid output

## Skill Structure

```
service-blueprint-skill/
├── SKILL.md              # This file (entry point)
├── METHODOLOGY.md        # How to think, facilitate, validate
├── SCHEMA.md             # JSON data structure
├── RENDERING.md          # HTML and Mermaid output specs
├── assets/
│   └── style.css         # HTML rendering styles
└── examples/
    ├── minimal.html      # 3-phase coffee shop
    ├── minimal.mermaid   # Same example in Mermaid
    ├── full.html         # 6-phase SaaS onboarding
    ├── full.mermaid      # Same example in Mermaid
    └── notation.html     # Visual reference guide
```

## When to Use This Skill

- User asks to create a "service blueprint"
- User wants to map customer journey with backend processes
- User needs to visualise frontstage/backstage service delivery
- User wants to identify moments of truth or failure points

## Output Format Selection

| Request | Format | File |
|---------|--------|------|
| "Create a service blueprint" | HTML | See RENDERING.md § HTML |
| "Service blueprint in Mermaid" | Mermaid | See RENDERING.md § Mermaid |
| "Blueprint for documentation" | Mermaid | Embeds in Markdown docs |
| "Interactive blueprint" | HTML | Full styling and legend |

## Generation Workflow

```
1. Understand scope (one scenario, one customer type)
       ↓
2. Structure data per SCHEMA.md
       ↓
3. Apply markers (moments of truth, failure points)
       ↓
4. Render per RENDERING.md (HTML or Mermaid)
       ↓
5. Verify against checklist
```

## Checklist (All Formats)

- [ ] Scope: One scenario, one customer type
- [ ] Structure: All 5 lanes, all 3 lines
- [ ] Time: Duration estimates per phase
- [ ] Flow: Arrows between phases and layers
- [ ] Analysis: Moments of truth (★) and failure points (!) marked
- [ ] Legend: Notation explained

## References

See METHODOLOGY.md for full citations. Key sources:
- Shostack, G.L. (1984). *Designing Services That Deliver*. Harvard Business Review
- Nielsen Norman Group service blueprinting articles
- UK Government Digital Service
- Practical Service Design (Flowers & Miller)
