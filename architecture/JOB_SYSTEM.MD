# Video Processing Pipeline

```
Input Video
      │
      ▼
Speech Analysis
      │
      ▼
Content Analysis
      │
      ▼
Story Engine
      │
      ▼
Timeline Planner
      │
      ▼
Motion Decision Engine
      │
      ▼
Motion Recipes
      │
      ▼
Motion Plugins
      │
      ▼
Motion Renderer
      │
      ▼
Render Plan
      │
      ▼
FFmpeg
      │
      ▼
Output Video
```

---

## Job Stages

### Stage 1

Analysis

- Speech
- Content
- Story

---

### Stage 2

Planning

- Timeline
- Motion
- Recipes

---

### Stage 3

Rendering

- Motion Plugins
- Motion Renderer
- FFmpeg

---

## Goal

Every stage performs a single responsibility and passes structured data to the next stage.

No rendering component should contain AI decision logic.
