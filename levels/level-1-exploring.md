# Level 1 — Exploring

O'Reilly skill: **Software Architecture** · [← Back to index](../README.md)
Source: https://learning.oreilly.com/skill/software-architecture/0642572295189/

Started: 2026-08-28

---

## How I use these notes

- One section per **competency** as I work through the skill.
- Capture the **concept**, a **short explanation in my own words**, and a **key takeaway**.
- Mark quiz status and log anything to revisit.
- Add references at the bottom.

---

## Level 1 Overview

- **43 Competencies** total across the skill · **15 competencies** in Level 1.
- Level 1 focus: *Architectural Thinking, Architecture Styles, Characteristics, Diagramming, and Data.*
- Current level: **Exploring**

Status legend: 🟢 Verified · 🟡 In progress · 🔴 Known gap · ⚪ Untested

---

## Level 1 Progress Tracker

| # | Competency | Status | Quiz | Notes |
|---|------------|--------|------|-------|
| 1.1 | Software Architecture vs Software Design | ⚪ | — | |
| 1.2 | Expectations of a Software Architect | ⚪ | — | |
| 1.3 | Modularity vs Granularity | ⚪ | — | |
| 1.4 | Identifying Architectural Styles | ⚪ | — | |
| 1.5 | Layered Monolithic Architecture Style | ⚪ | — | |
| 1.6 | Modular Monolith Architecture Style | ⚪ | — | |
| 1.7 | Microkernel Architecture Style | ⚪ | — | |
| 1.8 | Microservices Architecture Style | ⚪ | — | |
| 1.9 | Event-Driven Architecture Style | ⚪ | — | |
| 1.10 | Space-Based Architecture Style | ⚪ | — | |
| 1.11 | Understanding Architectural Characteristics | ⚪ | — | |
| 1.12 | Diagramming Software Architecture | ⚪ | — | |
| 1.13 | Data's Role in Software Architecture | ⚪ | — | |
| 1.14 | Understanding Data Topologies | ⚪ | — | |
| 1.15 | Understanding Database Types | ⚪ | — | |

---

## Level 1 — Competency Notes

### 1.1 — Software Architecture vs Software Design
> **Goal:** List the differences between software architecture and software design by outlining their scope and goals.

**Lessons:** Architectural Thinking · Architecture vs Design → Final Quiz

**Key ideas:**
- Architecture is high effort and strategic.
- Design is low effort and tactical.

**Takeaway:**
- Put your emphasis on the strategic, not the tactical.

Tactical = a specific action to remediate an immediate problem.

Strategy = a high-level visual to see and attack problems that could evolve in the short term.

Law of software architecture

1. Everything in software architecture is a trade-off.

2. Separation of concerns. How an architecture works is easy by reading the code. Documenting why a choice was made prevents future teams from blindly rewriting or breaking crucial context via Architecture Decision Records (ADR).

3. The law of change: the only constant in software is change.

---

### 1.2 — Expectations of a Software Architect
> **Goal:** Describe the responsibilities of a software architect within a development team.

**Lessons:** What is a Software Architect? · Expectations of a Software Architect → Final Quiz (70%)

**Key ideas:**
-

Collaboration, risk analysis, governance, facilitation, leadership, negotiation.

**Takeaway:**
1. Convert future decisions by prioritizing trade-offs.
2. Continually analyze the architecture and current technology, and recommend new solutions.
3. Analyze technology and industry trends, and stay current with them.

Too broad: application architect, security architect, network architect, solutions architect, system architect.
It will vary for every business.


---

### 1.3 — Modularity vs Granularity
> **Goal:** Define the significance of modularity, granularity, and separation of concerns.

**Lessons:** Business Drivers for Modularity · Technical Drivers for Modularity · Knowledge Check · Granularity Disintegrators · Granularity Integrators → Final Quiz (70%)

**Key ideas:**
- Modularity vs granularity:
Modularity = breaking the monolithc in pieces

Granularity = is how big are these components


- Separation of concerns:
- Disintegrators (reasons to break apart):
- Integrators (reasons to keep together):

**Takeaway:**
- 

---

### 1.4 — Identifying Architectural Styles
> **Goal:** List the primary differences between monolithic and distributed architectures.

**Lessons:** Monolithic vs Distributed Architecture · The 11 Fallacies of Distributed Computing → Final Quiz (70%)

**Key ideas:**
- Monolithic vs distributed:
- 11 Fallacies of distributed computing:

**Takeaway:**
- 

---

### 1.5 — Layered Monolithic Architecture Style
> **Goal:** Describe topologies and characteristics of the layered architectural style.

**Lessons:** Topology · Knowledge Check · Data Topology · Characteristics → Final Quiz (70%)

**Key ideas:**
- Topology:
- Data topology:
- Characteristics (ratings):

**Takeaway:**
- 

---

### 1.6 — Modular Monolith Architecture Style
> **Goal:** Describe topologies and characteristics of the modular monolith style.

**Lessons:** Topology · Knowledge Check · Data Topology · Characteristics → Final Quiz (70%)

**Key ideas:**
- 

**Takeaway:**
- 

---

### 1.7 — Microkernel Architecture Style
> **Goal:** Describe topologies and characteristics of the microkernel style.

**Lessons:** Topology · Knowledge Check · Data Topology · Characteristics → Final Quiz (70%)

**Key ideas:**
- Core system vs plug-in components:
- 

**Takeaway:**
- 

---

### 1.8 — Microservices Architecture Style
> **Goal:** Describe topologies and characteristics of the microservices style.

**Lessons:** Topology · Knowledge Check · Data Topology · Characteristics → Final Quiz (70%)

**Key ideas:**
- 

**Takeaway:**
- 

---

### 1.9 — Event-Driven Architecture Style
> **Goal:** Describe topologies and characteristics of the event-driven style.

**Lessons:** Topology · Exercise: Events vs Messages · Knowledge Check · Data Topology · Characteristics → Final Quiz (70%)

**Key ideas:**
- Broker vs mediator topology:
- Events vs messages:

**Takeaway:**
- 

---

### 1.10 — Space-Based Architecture Style
> **Goal:** Describe topologies and characteristics of the space-based style.

**Lessons:** Topology · Knowledge Check · Data Topology · Characteristics → Final Quiz (70%)

**Key ideas:**
- Tuple space / data grid, avoiding the database bottleneck:
- 

**Takeaway:**
- 

---

### 1.11 — Understanding Architectural Characteristics
> **Goal:** Identify key non-functional requirements (e.g., scalability, security) and recall their architectural implications.

**Lessons:** Understanding Architectural Characteristics → Final Quiz (70%)

**Key ideas:**
- Operational / structural / cross-cutting characteristics:
- 

**Takeaway:**
- 

---

### 1.12 — Diagramming Software Architecture
> **Goal:** Identify diagramming techniques to make solutions understandable to stakeholders.

**Lessons:** Diagramming Techniques · Representational Consistency → Final Quiz (70%)

**Key ideas:**
- Techniques (C4, UML, etc.):
- Representational consistency:

**Takeaway:**
- 

---

### 1.13 — Understanding Data's Role in Software Architecture
> **Goal:** Describe the role of data in software architecture and its influence.

**Lessons:** How Data Influences an Architecture → Final Quiz (70%)

**Key ideas:**
- 

**Takeaway:**
- 

---

### 1.14 — Understanding Data Topologies
> **Goal:** List the different types of data topologies that can be applied in an architecture.

**Lessons:** Data Topologies → Final Quiz (70%)

**Key ideas:**
- 

**Takeaway:**
- 

---

### 1.15 — Understanding Database Types
> **Goal:** Identify which database types align with various architectural styles.

**Lessons:** Database Types → Final Quiz (70%)

**Key ideas:**
- Relational / key-value / document / column / graph / time-series / NewSQL:
- 

**Takeaway:**
- 

---

## Findings & Insights

- 

---

## Open Questions

- [ ] 

---

## References

- O'Reilly Skill: Software Architecture — https://learning.oreilly.com/skill/software-architecture/0642572295189/
- _Fundamentals of Software Architecture_ — Mark Richards & Neal Ford
- _Software Architecture: The Hard Parts_ — Neal Ford, Mark Richards, et al.
