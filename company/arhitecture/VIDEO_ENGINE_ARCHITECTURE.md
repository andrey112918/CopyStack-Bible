## Motion Graphics Architecture

The rendering pipeline now follows this order:

Speech Analysis

↓

Video Analyst

↓

Subtitle Director

↓

Motion Director

↓

Asset Database

↓

Overlay Renderer

↓

Renderer

### Responsibilities

Video Analyst

* Detect important editing moments.
* Score words, phrases and sentences.

Subtitle Director

* Build subtitle instructions.
* Decide which keywords deserve emphasis.

Motion Director

* Decide which motion effect should accompany each subtitle.

Asset Database

* Select the correct visual asset for every motion type.

Overlay Renderer

* Load PNG/WebM/MOV assets.
* Position assets.
* Synchronize overlays with subtitle timing.

Renderer

* Combine subtitles, overlays and exported video into the final render.

