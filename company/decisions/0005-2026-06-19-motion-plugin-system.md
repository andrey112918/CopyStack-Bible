# Decision

Introduce Motion Plugin System V1.

---

## Motivation

Motion generation should become modular and extensible.

Each motion effect must exist as an independent plugin.

---

## Decision

Renderer resolves motion through MotionPluginRegistry.

Plugins build FilterGraph objects instead of directly modifying renderer logic.

---

## Benefits

- modular
- testable
- extensible
- AI friendly

---

## Future

Replace direct FFmpeg generation with:

Transform Engine

↓

Renderer Adapter

↓

Backend

This will remove FFmpeg-specific knowledge from AI components.
