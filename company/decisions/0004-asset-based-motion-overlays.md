# Decision 0004

## Title

Motion graphics will be built using reusable asset-based overlays instead of generated graphics.

---

## Status

Accepted

---

## Date

18 June 2026

---

## Context

The first versions of the Video Engine generated simple motion graphics directly through FFmpeg filters such as `drawbox` and other procedural effects.

Although this approach was sufficient for experimentation, it quickly revealed several limitations:

* limited visual quality
* difficult customization
* repetitive appearance
* poor support for branding
* difficult integration with professional motion graphics

To achieve professional editing quality similar to modern content creators, the rendering pipeline required a reusable asset-based solution.

---

## Decision

Motion graphics inside CopyStack will be implemented primarily through reusable visual assets rather than procedurally generated FFmpeg graphics.

Static and animated overlays will be stored inside dedicated asset libraries and selected dynamically by AI Employees during timeline generation.

Supported asset formats include:

* PNG
* WebM
* MOV
* future Blender exports
* future 3D assets

The renderer becomes responsible only for compositing these assets into the final video.

---

## Why

Asset-based graphics provide:

* significantly higher visual quality
* reusable design components
* consistent branding
* easier maintenance
* professional cinematic appearance

New motion graphics can be added simply by expanding the asset library without modifying rendering logic.

---

## Consequences

Motion graphics should never be hardcoded inside renderer components.

Future AI Employees should select assets instead of generating graphical primitives.

The Asset Library becomes one of the core resources of the Video Engine.

Future Localhost versions will manage this library through dedicated asset management interfaces.

---

## Alternatives Considered

### Procedural FFmpeg Graphics

Rejected because they are difficult to maintain and visually limited.

### Hardcoded Overlay Assets

Rejected because adding new assets would require renderer modifications.

### External Motion Software Only

Rejected because the renderer must remain capable of automatically producing complete videos without manual intervention.

---

## Reversible?

**NO**

Asset-based rendering becomes a permanent architectural principle of the Video Engine.
