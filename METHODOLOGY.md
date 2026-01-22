# Service Blueprint Methodology

How to think about, facilitate, and validate service blueprints.

---

## 1. What Service Blueprinting Is

> "A Service Blueprint is an Org Chart turned 90°. The point is to prioritise the experience of the customer rather than the structure of the organisation."
> — Cameron Tonkinwise, Professor, UTS School of Design

Service blueprinting reveals the organizational iceberg beneath every customer experience. Unlike journey maps (which show only what customers see), blueprints expose the choreography of people, systems, and processes that make experiences possible—or cause them to fail.

**Origin**: G. Lynn Shostack, Harvard Business Review, 1984, "Designing Services That Deliver"

### The Five Lanes

| Lane | What It Shows |
|------|---------------|
| **Physical Evidence** | Tangible/digital touchpoints customers encounter |
| **Customer Actions** | Steps customers take to use the service |
| **Frontstage Actions** | Employee/system activities visible to customers |
| **Backstage Actions** | Hidden activities supporting frontstage delivery |
| **Support Processes** | Internal systems and infrastructure enabling the service |

### The Three Lines

| Line | Boundary |
|------|----------|
| **Line of Interaction** | Customer ↔ Organization |
| **Line of Visibility** | What customers can/cannot see |
| **Line of Internal Interaction** | Contact staff ↔ Support staff |

---

## 2. Workshop Facilitation

### Team Composition

(NN/g research, n=97 practitioners)

- 4-6 core participants
- 1 facilitator per 12 attendees
- Must include: frontline staff, backstage operations, leadership with decision authority

> "Bring people who've never met before—they each owned different touchpoints"
> — Erika Flowers, Principal Service Designer, Intuit

### Scope Decision

- Target **8-12 customer actions**
- More than 15 = too granular
- Fewer than 5 = too abstract
- One blueprint = one scenario, one customer type

### Workshop Agendas

**Option A: Full Day** (NSW Government Digital Service)

| Block | Duration | Activity |
|-------|----------|----------|
| 1 | 60 min | Define scope, customer, scenario |
| 2 | 90 min | Map customer actions (diverge-converge) |
| 3 | 60 min | Lunch |
| 4 | 90 min | Map frontstage + backstage |
| 5 | 60 min | Add support processes, evidence |
| 6 | 30 min | Mark failures, dependencies, moments of truth |
| 7 | 30 min | Identify gaps, assign follow-ups |

**Option B: 60 Minutes** (Nava PBC)

| Block | Duration | Activity |
|-------|----------|----------|
| 1 | 10 min | Define service goal |
| 2 | 20 min | Map end users' steps and tools |
| 3 | 20 min | Map staff/management steps and tools |
| 4 | 10 min | Identify gaps, assumptions, questions |

### Core Technique: Diverge-Converge

**Step 1 — Silent generation (10 min)**
Each participant writes sticky notes independently. No discussion.

**Step 2 — Post and cluster (10 min)**
Everyone posts notes simultaneously. Facilitator groups similar items.

**Step 3 — Discuss and align (15 min)**
Walk through clusters. Resolve conflicts. Identify gaps.

### Five Questions to Drive Each Lane

| Lane | Driving Question |
|------|------------------|
| **Customer Actions** | "What is the customer *doing* at this moment?" |
| **Frontstage** | "What does the customer *see us doing* in response?" |
| **Backstage** | "What happens *behind the scenes* to enable that?" |
| **Support Processes** | "What *systems, policies, or teams* make that possible?" |
| **Physical Evidence** | "What *tangible thing* does the customer see or receive?" |

---

## 3. Identifying What Matters

### Moments of Truth

**Definition** (NN/g): Occasions when customers judge your quality and make decisions about future purchases.

**The asymmetry**: It takes 12 positive moments to counter 1 failed moment.

**Three identification methods**:

1. **Line of interaction scan**
   - Every point where customer crosses into your world = potential moment of truth
   - Ask: "If this goes wrong, does the customer notice immediately?"

2. **Emotional peak/valley analysis**
   - Plot emotional highs and lows across the journey
   - Peaks and valleys = critical moments

3. **The "would they tell someone" test**
   - Ask: "Would a customer tell a friend about this moment—good or bad?"
   - If yes → moment of truth

### Failure Points

**Definition** (Shostack): Any point within the service encounter that has potential to affect customer satisfaction or quality.

> "Poor user experiences are often due to an internal organizational shortcoming—a weak link in the ecosystem."
> — Sarah Gibbons, NN/g

**Five questions to surface failures**:

1. "What happens if this step takes twice as long as expected?"
2. "What happens if the information passed here is wrong?"
3. "What happens if the person responsible is unavailable?"
4. "What happens if the system is down?"
5. "What happens if the customer doesn't understand what to do?"

### Dependencies

**Visual convention** (Vaimo):
- Single arrow → = one-way handoff
- Double arrow ↔ = codependence / negotiation required

**Questions**:
1. "Who needs to complete their work before this can start?"
2. "Who is waiting on the output of this step?"
3. "If this fails, what else breaks?"

### Prioritising: Dot Voting

1. Give each participant 2 votes
2. Vote on most significant issues
3. Tally votes
4. Address highest-vote items first

---

## 4. Validation

> "How things are supposed to be done is rarely how they're done. You need to discover and document the latter."
> — Nielsen Norman Group

### Validation Sequence (Nava PBC)

| Stage | Activity | Participants |
|-------|----------|--------------|
| 1 | Workshop first draft | Small core team |
| 2 | Walk-through validation | Key users and stakeholders |
| 3 | Detail enrichment | Tech, policy, operations teams |
| 4 | Application | Use discoveries to align and improve |

**Critical rule**: Never email a blueprint for review. Validate in person.

### Validation Methods

Minimum: Two research methods with direct observation:
- Contextual inquiry
- Staff interviews
- Direct observation
- Diary studies

### Three Questions for Frontline Validation

1. "Does this match what actually happens, or what's supposed to happen?"
2. "What's missing that you deal with regularly?"
3. "Where do things most often go wrong?"

---

## 5. Anti-Patterns

### ❌ Treating blueprints as deliverables

> "Service Blueprints are an early stage working tool and should never be the basis of a communication to clients."
> — Cameron Tonkinwise

**Fix**: Use for internal alignment. Create separate artifacts for stakeholders.

### ❌ Scope creep

**Fix**: One blueprint = one scenario. Split complex services.

### ❌ Organizational isolation

**Finding** (NN/g): Fewer than half include leadership, support, marketing, sales.

**Fix**: Cross-functional participation is mandatory.

### ❌ Premature fidelity

> "The fidelity should mirror where you are; the earlier, the lower."
> — Nielsen Norman Group

**Fix**: Start with sticky notes. Digitise when structure stabilises.

### ❌ Facilitator-as-participant

**Fix**: Choose one role. Bring a neutral facilitator if you have domain expertise.

### ❌ Blueprinting new services

> "Use service blueprints for existing services. Not for new services or ideation."
> — Wales Centre for Digital Public Services

**Fix**: Journey map and prototype first. Blueprint after initial launch.

---

## 6. Maintenance

### Three States (NSW Government)

| State | Purpose |
|-------|---------|
| **Current State** | How customers experience the service today |
| **Target State** | Planned improvements |
| **Future State** | Aspirational "North Star" |

### Cadence (NN/g)

1. Update after each significant service change
2. Schedule 6-month review
3. Include version number and date on artifact
4. Archive old versions for decision history

### Team Integration (UK GDS)

> "If the team uses the blueprint as part of their planning rituals it becomes a tool that helps build a case for stopping something, starting something new or continuing longer."
> — Lina Nilsson, UK Government Digital Service

---

## References

### Methodology
- Shostack, G.L. (1984). Designing Services That Deliver. *Harvard Business Review*
- Flowers, E. & Miller, M. Practical Service Design. practicalservicedesign.com
- Gibbons, S. Service Blueprints: Definition. Nielsen Norman Group

### Government Frameworks
- NSW Government Digital Service Toolkit. digital.nsw.gov.au
- UK Government Digital Service. services.blog.gov.uk
- Wales Centre for Digital Public Services. digitalpublicservices.gov.wales
- Singapore GovTech. tech.gov.sg
- Nava PBC Facilitation Guide. navapbc.com

### Critical Perspectives
- Tonkinwise, C. Hacking Service Blueprints. medium.com/@camerontw
- Vaimo. What is a Service Blueprint. vaimo.com
- Make It Clear. Service Blueprinting. makeitclear.com
