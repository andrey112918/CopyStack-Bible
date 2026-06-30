# Decision #0013 — AI Director Becomes the Single Source of Truth

## Status

Accepted

## Date

2026-06-30

---

# Context

As the Video Engine grew, multiple independent systems started making cinematic decisions.

Examples included:

- Motion Director
- Motion Decision Engine
- Impact Event Planner
- Music Motion Adapter
- Timeline motion generation

Although each system worked individually, together they produced duplicated or conflicting visual decisions.

Examples:

- Multiple motion layers fighting each other.
- Camera emphasis generated from one system while motion came from another.
- Random-looking visual density.
- Inconsistent cinematic rhythm.

The generated videos no longer reflected one intentional editing strategy.

---

# Decision

CopyStack will move toward a centralized cinematic architecture.

The AI Director becomes the primary decision maker.

Instead of every subsystem deciding independently, future employees will consume a shared DirectorDecisionPackage.

Examples:

AI Director

↓

Camera Director

↓

Motion Director

↓

Subtitle Director

↓

Effects Director

↓

SFX Director

↓

B-roll Director

↓

Music Director

Each director becomes an executor rather than an independent decision maker.

---

# Why

Benefits include:

- Consistent editing philosophy.
- Better coordination between camera, motion and subtitles.
- Easier debugging.
- Reusable cinematic recipes.
- Better scalability for future employees.

Instead of optimizing individual effects, the system optimizes complete cinematic decisions.

---

# Consequences

Positive:

- Cleaner generated videos.
- Less duplicated motion.
- Shared cinematic language.
- Easier future expansion.

Trade-offs:

- AI Director becomes a critical component.
- Future directors must follow the shared decision package.

---

# Alternatives Considered

## Independent Directors

Rejected.

Although flexible, this approach produced conflicting cinematic decisions.

## Hardcoded Timeline Rules

Rejected.

Too difficult to maintain as the Video Engine grows.

---

# Reversible

Yes.

Individual directors can temporarily make standalone decisions if the AI Director becomes unavailable, but this should only be considered a fallback mode.
