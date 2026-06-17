# ADR-0004

# Asset-Based Motion Graphics

## Status

Accepted

## Context

The original implementation used FFmpeg drawbox filters to generate motion graphics.

Although functional, this approach has several limitations:

* Poor visual quality.
* Difficult to scale.
* Limited animation capabilities.
* Cannot support 3D assets.

## Decision

Motion graphics will no longer be generated procedurally with drawbox.

Instead, CopyStack will use an Asset-Based Motion System.

Pipeline:

Motion Director

↓

Asset Director

↓

Overlay Renderer

↓

Renderer

Assets may include:

* PNG
* WebM
* MOV with Alpha
* Blender exports
* Future 3D assets

## Consequences

Advantages:

* Better visuals.
* Easy expansion.
* Reusable asset library.
* Future support for 3D motion graphics.
* Cleaner renderer architecture.
