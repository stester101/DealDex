# Deal Dex 2 — playable foundation

This is an **early prototype**, not a completed sequel. It is isolated under `sequel/` so the original Deal Dex remains intact.

## Run
Serve the repository locally (`python3 -m http.server 8000`) and visit `/sequel/`. ES modules require an HTTP server. GitHub Pages can host this directory.

## Implemented
- Canvas pixel-art coastal map and following camera
- Touch and keyboard movement, collisions, grass encounters
- Prototype battle, capture, experience and money loop
- Party, Dex and local save
- PWA manifest

## Not yet implemented
Production sprites and tile art; original game's full Dex, moves and battle mechanics; story, NPCs, quests, map transitions; balancing; accessibility audit; Android APK and signing. The current placeholder battle does not represent the original battle engine.

## Android delivery
Use Capacitor to wrap the built web app, with an Android SDK and Gradle to produce a debug APK, then sign a release APK. Do not ship a release build without testing offline assets, storage, screen layouts, performance, back-button handling and save migrations.

## Design direction
The generated promotional concept is a visual target, **not** a spritesheet or gameplay screenshot. Recreate individual original pixel assets with a consistent 16/32px tile grid, layered shadows and animated water. Import content from Deal Dex 1 through a validated extraction pipeline rather than duplicating its monolithic React/Babel runtime.

## Next engineering milestones
1. Extract canonical Dex, move, type, encounter, item and evolution data from V1 into JSON with tests.
2. Build deterministic turn-based combat with unit tests and full type/status/move support.
3. Implement authored region maps, NPCs, quests, checkpoints and navigation.
4. Replace procedural placeholders with consistent pixel assets and animation sheets.
5. Add save schema versioning, accessibility, sound and offline caching.
6. Add Capacitor Android project and automated APK build.
7. Run playtests and content/balance validation before release.
