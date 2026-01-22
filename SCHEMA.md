# Service Blueprint Schema

Structured JSON format for service blueprint data. Use this schema to define blueprint content before rendering to HTML or Mermaid.

---

## Schema Definition

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "ServiceBlueprint",
  "type": "object",
  "required": ["title", "phases"],
  "properties": {
    "title": {
      "type": "string",
      "description": "Blueprint title"
    },
    "subtitle": {
      "type": "string",
      "description": "Optional subtitle or scope description"
    },
    "version": {
      "type": "string",
      "description": "Version number (e.g., '1.0', '2.1')"
    },
    "lastUpdated": {
      "type": "string",
      "format": "date",
      "description": "ISO date of last update"
    },
    "variants": {
      "type": "array",
      "description": "For comparative blueprints, define variant labels",
      "items": {
        "type": "object",
        "properties": {
          "id": { "type": "string" },
          "label": { "type": "string" },
          "color": { "type": "string", "description": "CSS color for badge" }
        }
      }
    },
    "phases": {
      "type": "array",
      "minItems": 3,
      "maxItems": 12,
      "items": { "$ref": "#/definitions/Phase" }
    }
  },
  "definitions": {
    "Phase": {
      "type": "object",
      "required": ["name", "customer"],
      "properties": {
        "name": { "type": "string" },
        "duration": { "type": "string", "description": "e.g., '1-2 days'" },
        "durationByVariant": {
          "type": "object",
          "additionalProperties": { "type": "string" }
        },
        "evidence": {
          "type": "array",
          "items": { "$ref": "#/definitions/Action" }
        },
        "customer": {
          "type": "array",
          "items": { "$ref": "#/definitions/Action" }
        },
        "frontstage": {
          "type": "array",
          "items": { "$ref": "#/definitions/Action" }
        },
        "backstage": {
          "type": "array",
          "items": { "$ref": "#/definitions/Action" }
        },
        "support": {
          "type": "array",
          "items": { "$ref": "#/definitions/Action" }
        },
        "arrowType": {
          "type": "string",
          "enum": ["single", "double", "none"],
          "default": "single",
          "description": "Arrow to next phase: single (→), double (↔), none"
        }
      }
    },
    "Action": {
      "type": "object",
      "required": ["text"],
      "properties": {
        "text": { "type": "string" },
        "variant": { "type": "string", "description": "Variant ID if specific to one path" },
        "momentOfTruth": { "type": "boolean", "default": false },
        "failurePoint": { "type": "boolean", "default": false },
        "muted": { "type": "boolean", "default": false, "description": "Inactive/N/A styling" }
      }
    }
  }
}
```

---

## Example: Minimal Blueprint

```json
{
  "title": "Coffee Shop Order",
  "subtitle": "3-phase minimal example",
  "version": "1.0",
  "lastUpdated": "2025-01-22",
  "phases": [
    {
      "name": "ORDER",
      "duration": "1-2 min",
      "evidence": [
        { "text": "Menu board" },
        { "text": "POS terminal" }
      ],
      "customer": [
        { "text": "Review menu", "momentOfTruth": true },
        { "text": "Place order" },
        { "text": "Pay" }
      ],
      "frontstage": [
        { "text": "Greet customer", "momentOfTruth": true },
        { "text": "Take order" },
        { "text": "Process payment" }
      ],
      "backstage": [
        { "text": "Print ticket" }
      ],
      "support": [
        { "text": "POS system" },
        { "text": "Payment gateway" }
      ]
    },
    {
      "name": "PREPARE",
      "duration": "3-5 min",
      "evidence": [
        { "text": "Order ticket" },
        { "text": "Coffee machine" }
      ],
      "customer": [
        { "text": "Wait" }
      ],
      "frontstage": [
        { "text": "Call name when ready" }
      ],
      "backstage": [
        { "text": "Pull espresso shot", "failurePoint": true },
        { "text": "Steam milk" },
        { "text": "Assemble drink" }
      ],
      "support": [
        { "text": "Coffee machine" },
        { "text": "Bean supply", "failurePoint": true }
      ]
    },
    {
      "name": "DELIVER",
      "duration": "30 sec",
      "arrowType": "none",
      "evidence": [
        { "text": "Branded cup" },
        { "text": "Receipt" }
      ],
      "customer": [
        { "text": "Collect drink", "momentOfTruth": true },
        { "text": "Leave" }
      ],
      "frontstage": [
        { "text": "Hand over drink" },
        { "text": "Thank customer" }
      ],
      "backstage": [
        { "text": "Quality check" }
      ],
      "support": [
        { "text": "Cup inventory" }
      ]
    }
  ]
}
```

---

## Example: Comparative Blueprint (with Variants)

```json
{
  "title": "SaaS Customer Onboarding",
  "subtitle": "Comparing Self-Serve and Enterprise paths",
  "version": "1.0",
  "lastUpdated": "2025-01-22",
  "variants": [
    { "id": "ss", "label": "SS", "color": "#dbeafe" },
    { "id": "en", "label": "EN", "color": "#fef3c7" }
  ],
  "phases": [
    {
      "name": "SIGN UP",
      "durationByVariant": {
        "ss": "5 min",
        "en": "1-2 weeks"
      },
      "evidence": [
        { "text": "Landing page" },
        { "text": "Pricing page" },
        { "text": "Contract", "variant": "en" }
      ],
      "customer": [
        { "text": "Visit website", "momentOfTruth": true },
        { "text": "Create account", "variant": "ss" },
        { "text": "Request demo", "variant": "en" }
      ],
      "frontstage": [
        { "text": "Send welcome email", "momentOfTruth": true },
        { "text": "Schedule demo", "variant": "en" },
        { "text": "Assign CSM", "variant": "en" }
      ],
      "backstage": [
        { "text": "Provision tenant" },
        { "text": "Lead scoring" },
        { "text": "Contract negotiation", "variant": "en", "failurePoint": true }
      ],
      "support": [
        { "text": "Auth system" },
        { "text": "Tenant provisioning" },
        { "text": "CRM integration" }
      ]
    }
  ]
}
```

---

## Schema Usage Notes

### Markers

| Property | Visual | Purpose |
|----------|--------|---------|
| `momentOfTruth: true` | ★ (red) | Customer perception crystallises here |
| `failurePoint: true` | ! (yellow) | Dependency or risk point |
| `muted: true` | Dashed border | Inactive or N/A for this scenario |

### Arrow Types

| `arrowType` | Visual | When to Use |
|-------------|--------|-------------|
| `"single"` | → | Default one-way handoff |
| `"double"` | ↔ | Negotiation or agreement required |
| `"none"` | (blank) | Last phase (no next phase) |

### Variants

For comparative blueprints:
1. Define variants array with `id`, `label`, `color`
2. Tag actions with `variant: "id"` to show only for that path
3. Use `durationByVariant` for phase-level timing differences

### Validation Rules

1. **3-12 phases** (fewer than 3 lacks context; more than 12 is too granular)
2. **Customer actions required** for each phase
3. **Last phase** should have `arrowType: "none"`
4. **At least one moment of truth** in the blueprint
5. **Failure points** should exist in backstage or support lanes
