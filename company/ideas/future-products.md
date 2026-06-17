## Intelligent Media Selector

When CopyStack moves to localhost and the main system is stable, the Video Engine should be able to analyze a large library of user-provided media and choose the best materials for an edit.

Example:

The user provides:

* 100 photos
* 20 videos

CopyStack should automatically:

* analyze every photo
* analyze every video
* detect the best moments inside each video
* identify which photos are most relevant to the topic
* identify which clips are most useful for the final edit
* explain why each selected asset was chosen
* explain why the rejected assets were not selected

The system should not choose media randomly.

It should decide based on:

* relevance to the script
* visual quality
* emotional impact
* clarity
* topic match
* brand fit
* scene usefulness
* potential for B-roll
* potential for hooks
* potential for transitions
* uniqueness

Future employee idea:

Media Selection Director

Responsibilities:

* scan all available media
* rank photos and videos
* select the best assets for the edit
* create a selection report
* explain every important decision

Example output:

Selected:

* photo_12.jpg
  Reason: Best visual match for the topic, clear composition, strong emotional impact.

* clip_04.mp4 from 00:12 to 00:18
  Reason: Contains the most relevant moment for the section about client results.

Rejected:

* photo_31.jpg
  Reason: Low relevance to the current script and weak visual quality.

* clip_09.mp4
  Reason: Good quality, but not aligned with the message of the edit.

This feature would allow CopyStack to act more like a real editor, not only generating effects but also choosing the best creative material from a large media library.

2026-06-17


## Localhost Progress Showcase

When CopyStack moves to localhost, the app should include a section, tab, or popup for daily progress showcases.

Example:

Day 2

The section should store:

* the script for the video
* what should be shown on screen while speaking
* project progress
* key achievements
* next steps

This will allow CopyStack to document the build journey directly inside the product.

## Day 2 Showcase Script Notes

"Astăzi am lucrat aproape șase ore..."
Show the project structure in VS Code.

"Până acum sistemul putea doar să genereze subtitrări."
Show a clip with subtitles.

"Acum începe să înțeleagă videoclipul."
Show Video Analyst and Editing Report.

"Motion Director decide..."
Show the overlay synchronized with CopyStack.

"Biblioteca de asset-uri..."
Show the assets/motion folder.

"AI Video Operating System"
Zoom in on the AI Employees architecture or project structure.

## Script Helper

Future feature idea:

CopyStack should include a Script Helper.

The user tells CopyStack what they want to create using the materials they provide.

If the spoken content, footage, photos, or clips are not enough, CopyStack should help improve the idea and suggest what is missing.

The Script Helper should be able to:

* understand the goal of the video
* analyze the available materials
* detect missing context
* suggest better script angles
* improve weak spoken content
* help turn raw materials into a stronger video concept
* guide the user on what extra footage, photos, or voiceover would improve the edit

2026-6-17

## Production Assistant Rules

The Production Assistant is responsible for deciding how every scene should be produced.

The selected production method is not a suggestion.

It is the workflow that CopyStack will execute.

### Raw Creator Footage

The creator records the scene exactly as instructed.

The final edit uses the raw recording with only minimal processing.

### Engine Edit

When this option is selected, the creator only provides the required materials.

Examples:

* raw camera footage
* photos
* screen recordings
* logos
* product images

CopyStack is fully responsible for producing the final scene.

The engine automatically decides and generates:

* subtitles
* cuts
* B-roll
* transitions
* motion graphics
* sound effects
* camera movements
* overlays
* animations
* color adjustments
* pacing

If the Production Assistant chooses Engine Edit, the final result must be rendered by CopyStack.

Manual editing is no longer required.

### Screen Recording

The creator records the required workflow.

CopyStack edits and enhances the recording automatically.

### Mixed Production

The creator records only the parts that require human presence.

Everything else is produced automatically by CopyStack.

Examples:

* B-roll
* transitions
* overlays
* motion graphics
* assets
* captions
* effects

## Design Principle

The user should never wonder:

"Should I edit this myself?"

The Production Assistant makes that decision.

Once a production method is selected, CopyStack is responsible for executing it.

2026-6-17
