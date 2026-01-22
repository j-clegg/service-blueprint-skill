# Service Blueprint Skill

A Claude skill for generating professional service blueprints following the Flowers & Miller methodology and NN/g (Nielsen Norman Group) visual standards.

## What is a Service Blueprint?

A service blueprint visualises the relationships between service components—people, processes, and systems—tied to touchpoints in a customer journey. Unlike journey maps, blueprints expose the organisational iceberg: the backstage processes and support systems that make experiences possible.

## Skill Structure

```
service-blueprint-skill/
├── SKILL.md              # Entry point and quick reference
├── METHODOLOGY.md        # How to think, facilitate, validate
├── SCHEMA.md             # JSON data structure for blueprints
├── RENDERING.md          # HTML and Mermaid output specs
├── assets/
│   └── style.css         # HTML rendering styles
└── examples/
    ├── minimal.html      # 3-phase coffee shop (HTML)
    ├── minimal.mermaid.md # Same example (Mermaid)
    ├── full.html         # 6-phase SaaS onboarding (HTML)
    ├── full.mermaid.md   # Same example (Mermaid)
    └── notation.html     # Visual reference guide
```

## Quick Start

1. **Understand the methodology** → Read `METHODOLOGY.md`
2. **Structure your data** → Follow `SCHEMA.md`
3. **Choose output format** → See `RENDERING.md`

## Output Formats

| Format | Best For | File |
|--------|----------|------|
| **HTML** | Standalone artifacts, presentations, full styling | `RENDERING.md § HTML` |
| **Mermaid** | Documentation, Markdown embedding, version control | `RENDERING.md § Mermaid` |

### Format Comparison

| Aspect | HTML | Mermaid |
|--------|------|---------|
| Markers | Styled ★ and ! circles | Text suffixes ★ ❗ |
| Badges | Colored spans | Text suffixes (SS) (EN) |
| Legend | Full visual | Markdown table |
| Complexity | Any size | Best for 3-6 phases |

## Key Features

### Methodology (from practitioners)
- Workshop facilitation guides (60 min and full-day agendas)
- Questions for surfacing moments of truth and failure points
- Validation sequence and anti-patterns to avoid
- Citations from NN/g, UK GDS, Nava PBC, and more

### Schema
- JSON structure for programmatic generation
- Support for variants (comparing service paths)
- Marker definitions (momentOfTruth, failurePoint)
- Arrow types (single, double, none)

### Rendering
- Consistent CSS patterns that work
- Mermaid block diagrams matching HTML styling
- Common issues and fixes documented

## Examples

### Minimal (3-phase)
Coffee shop order flow. Simple structure, easy to understand.
- `examples/minimal.html`
- `examples/minimal.mermaid.md`

### Full (6-phase)
SaaS customer onboarding comparing Self-Serve vs Enterprise paths.
- `examples/full.html`
- `examples/full.mermaid.md`

### Notation Reference
Visual guide to all arrows, markers, and styling.
- `examples/notation.html`

## Methodology Sources

- Shostack, G. Lynn (1984). *Designing Services That Deliver*. Harvard Business Review
- Flowers, E. & Miller, M. *Practical Service Design*
- Nielsen Norman Group service blueprinting articles
- UK Government Digital Service
- NSW Government Digital Service Toolkit
- Nava PBC Facilitation Guide
- Tonkinwise, C. *Hacking Service Blueprints*

## License

MIT
