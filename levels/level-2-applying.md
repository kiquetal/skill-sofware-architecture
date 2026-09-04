# Level 2 — Applying

O'Reilly skill: **Software Architecture** · [← Back to index](../README.md)
Source: https://learning.oreilly.com/skill/software-architecture/0642572295189/

Started: 2026-08-29

---

## How I use these notes

- One section per **competency** as I work through the skill.
- Capture the **concept**, a **short explanation in my own words**, and a **key takeaway**.
- Mark quiz status and log anything to revisit.
- Add references at the bottom.

---

## Level 2 Overview

- **Level 2 focus:** *Designing, identifying components, coupling, and deep dives into architectures.*
- Current level: **Applying**

Status legend: 🟢 Verified · 🟡 In progress · 🔴 Known gap · ⚪ Untested

---

## Level 2 Progress Tracker

| # | Competency | Status | Quiz | Notes |
|---|------------|--------|------|-------|
| 2.1 | Designing Software Architectures | 🟢 | — | |
| 2.2 | Identifying Software Architecture Components | 🟢 | — | |
| 2.3 | Coupling Components in Software Architecture | 🟢 | — | |
| 2.4 | Understanding the Principle of Least Knowledge | 🟢 | — | |
| 2.5 | Component Identification Techniques | 🟢 | — | |
| 2.6 | Architecture to Domain Isomorphism | ⚪ | — | |
| 2.7 | Examining Layered Monolithic Architectures | 🟡 | — | |
| 2.8 | Examining Modular Monolithic Architectures | ⚪ | — | |
| 2.9 | Examining Microkernel Architectures | ⚪ | — | |
| 2.10 | Examining Microservices Architecture | ⚪ | — | |
| 2.11 | Examining Event-Driven Architectures | ⚪ | — | |
| 2.12 | Examining Space-Based Architectures | ⚪ | — | |

---

## Level 2 — Competency Notes

### 2.1 — Designing Software Architectures
> **Goal:** Interpret the relationship between logical components and the structure of the corresponding source code.

**Lessons:** Designing Software Architectures → Final Quiz (70%)

**Key ideas:**
-

The "physical" is just what are being configured or something like instances

**Takeaway:**
-

---

### 2.2 — Identifying Software Architecture Components
> **Goal:** Classify system components and discuss how user stories relate to them.

**Lessons:** Identifying Components → Final Quiz (70%)

**Key ideas:**
-

Identify initial core components -> asign user stories to components ->  analyze roles and responsability -> analyze architecture characteristics -> refactor or add components

**Takeaway:**
-

---

### 2.3 — Coupling Components in Software Architecture
> **Goal:** Summarize the three types of coupling in software architecture.

**Lessons:** Three Types of Coupling in Software Architecture → Final Quiz (70%)

**Key ideas:**
- **Afferent Coupling (Ca):** "Incoming" coupling. The number of components that depend *on* this component.
  ```text
  [ A ] \
         --> [ Component ]
  [ B ] /
  (A and B depend ON "Component" -> High Ca)
  ```
- **Efferent Coupling (Ce):** "Outgoing" coupling. The number of components this component depends *on*.
  ```text
           /-> [ C ]
  [ Component ]
           \-> [ D ]
  ("Component" depends ON C and D -> High Ce)
  ```
- **Abstract Coupling:** Coupling through interfaces rather than concrete implementations.

**Takeaway:**
- Afferent and efferent coupling analysis helps quantify the stability of components. The instability metric (I = Ce / (Ce + Ca)) guides how we manage dependencies to minimize cascading changes and improve system maintainability.

---

### 2.4 — Understanding the Principle of Least Knowledge
> **Goal:** Discuss how the Law of Demeter (Principle of Least Knowledge) minimizes coupling in architectural designs.

**Lessons:** The Law of Demeter → Final Quiz (70%)

**Key ideas:**
- "A service or component should have limited knowledge about other services or components; it should only talk to its immediate friends."
- This is also known as the Principle of Least Knowledge, which dictates that a component should not traverse the internal structure of its associates to reach deeper objects.
- **Architectural Use Case (Violation):** An `OrderService` needs to update shipping status. Instead of calling `ShippingService`, it bypasses it and calls `WarehouseService` directly to update the package status, because it knows that `WarehouseService` is an internal dependency of `ShippingService`.
- **Architectural Use Case (Fix):** `OrderService` calls `ShippingService`. `ShippingService` manages the orchestration with `WarehouseService` internally. `OrderService` remains ignorant of `WarehouseService`'s existence or API.

```text
// Violation (Architectural "Train Wreck")
[ OrderService ] ---> [ ShippingService ] ---> [ WarehouseService ]
(OrderService knows about and calls the internal WarehouseService)

// Fix (LoD compliant - Encapsulation)
[ OrderService ] ---> [ ShippingService ]
                             |
                             v
                    [ WarehouseService ]
```

**Takeaway:**
- Applying the Law of Demeter reduces architectural coupling. By forcing components to interact only through defined APIs of direct dependencies, we maintain encapsulation, allowing internal components to be refactored without breaking higher-level service contracts.


Everything is a trade-off

Order was the centralized so that would be the benefit

When we change to loouse coupling we just depende on another and aother components.


---

### 2.5 — Component Identification Techniques
> **Goal:** Demonstrate the creation of a logical architecture and classify its core components.

**Lessons:** Component Identification Techniques → Final Quiz (70%)

**Key ideas:**
- **KATA techniques:**
  - The entity trap: THIS IS THE GO-TO ARCHITECTURE, just do not trust.
- **The Entity Trap (Expanded):** Avoid the common mistake of simply mapping database tables/entities directly to architectural components. Entities are data holders; components should be defined by **behavior** and **responsibilities**.
- **User Story Decomposition:** Map user stories to specific components. If a user story spans too many components, that is a smell suggesting your components might be too granular or improperly bounded.
- **Component Classification:** 
  - **Core Components:** Handle the primary domain logic.
  - **Supporting Components:** Provide utility functions (logging, data validation, etc.).
  - **Infrastructure Components:** Handle cross-cutting concerns (DB access, messaging).
- **Iterative Refinement:** Start with a high-level view (the "initial core components"), map functionality, analyze for cohesion and coupling (afferent/efferent), and refactor.

**Takeaway:**
- Don't just design for data—design for *behavior*. A robust component identification strategy requires balancing domain logic encapsulation with architectural characteristics (scalability, maintainability, etc.).

---

### 2.6 — Architecture to Domain Isomorphism
> **Goal:** Explain how domain isomorphism correlates with architectural styles.

**Lessons:** Architecture to Domain Isomorphism → Final Quiz (70%)

Isomorphism: isos meaning equal morphe = form or shape.

Does the shape of architecture match the shape  of the problem domain?

Styles are named topologies, while patterns are contextual solutions to problems.

Architectura topology the generic shape or structure of an architecture

**Key ideas:**
-

**Takeaway:**
-

---

### 2.7 — Examining Layered Monolithic Architectures
> **Goal:** Explain the topology specifics, governance techniques, cloud considerations, common risks, team topologies, and examples of layered architectures.

**Lessons:** Deep Dive into Layered Monolithic Architecture → Final Quiz (70%)

**Key ideas:**
- **Team enabled:** Facilitates concurrent work by different teams on different layers.
- **Big ball of mud:** A significant risk if layer boundaries are not strictly enforced and layers are left open.
- **Sinkhole architecture:** A risk where a request passes through a layer without any logic or transformation, just acting as a "pass-through" (a sinkhole).
- **Open/Closed Layers:**
  - **Closed Layer:** A request must go through the layer immediately below it.
  - **Open Layer:** A request can skip a layer to access the one below it.

```text
// Closed Layer (Strict - More secure/controlled)
+--------------+
|      UI      |
+--------------+
       |
+--------------+
|   Business   |
+--------------+
       |
+--------------+
| Persistence  |
+--------------+

// Open Layer (Flexible - Can skip a layer)
+--------------+
|      UI      |
+--------------+
  |    |
  |    +--------+ (skips Business)
  v             |
+--------------+v
|   Business   +--------------+
+--------------+              |
       |                      |
+--------------+--------------+
| Persistence  |
+--------------+
```


We can bypass some layers

Separation of concerns in trumbles.


**Takeaway:**
- Closed layers provide better encapsulation and easier change management, but open layers can improve performance by reducing overhead in simple systems. Trade-offs!

Separation of concerns in trumbles.

---

### 2.8 — Examining Modular Monolithic Architectures
> **Goal:** Explain the topology specifics, governance techniques, cloud considerations, common risks, team topologies, and examples of modular monolithic architectures.

**Lessons:** Deep Dive into Modular Monolithic Architecture → Final Quiz (70%)

**Key ideas:**
-

**Takeaway:**
-

---

### 2.9 — Examining Microkernel Architectures
> **Goal:** Explain the topology specifics, governance techniques, cloud considerations, common risks, team topologies, and examples of microkernel architectures.

**Lessons:** Deep Dive into Microkernel Architecture → Final Quiz (70%)

**Key ideas:**
-

**Takeaway:**
-

---

### 2.10 — Examining Microservices Architecture
> **Goal:** Explain the topology specifics, governance techniques, cloud considerations, common risks, team topologies, and examples of microservices architecture.

**Lessons:** Deep Dive into Microservices Architecture → Final Quiz (70%)

**Key ideas:**
-

**Takeaway:**
-

---

### 2.11 — Examining Event-Driven Architectures
> **Goal:** Explain the topology specifics, governance techniques, cloud considerations, common risks, team topologies, and examples of event-driven architectures.

**Lessons:** Deep Dive into Event-Driven Architecture → Final Quiz (70%)

**Key ideas:**
-

**Takeaway:**
-

---

### 2.12 — Examining Space-Based Architectures
> **Goal:** Explain the topology specifics, governance techniques, cloud considerations, common risks, team topologies, and examples of space-based architectures.

**Lessons:** Deep Dive into Space-Based Architecture → Final Quiz (70%)

**Key ideas:**
-

**Takeaway:**
-

---

## References

- O'Reilly Skill: Software Architecture — https://learning.oreilly.com/skill/software-architecture/0642572295189/
