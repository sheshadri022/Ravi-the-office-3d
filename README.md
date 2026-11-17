# Ravi Kumar · The Office (3D)

Interactive 3D portfolio for Ravi Kumar, Group Vice President – Finance, Miles Education.

A low-poly office inside a living city block, built with Three.js. A guided tour follows a visitor through security and reception to Ravi's cabin, then walks room by room through his career, narrated in his own voice. "Exit demo" switches to free explore mode.

## Game Mode (`/game`)
Play as the visitor: WASD / joystick, check in at reception, meet Ravi, collect 5 career milestones, finish for a time + XP score.
Leaderboard: Supabase Edge Function `leaderboard` (project `ravi-office-game`) storing rows in `public.scores`. The function validates scores server-side, so no API key ships to the browser. Endpoint is set in `game/config.js`.

## Rooms
01 Reception · 02 Milestone Wall · 03 Reporting Studio · 04 Automation Lab · 05 Deal Room · 06 Global Atrium · 07 Ravi's Cabin

## Run locally
Static site, no build step:

    python3 -m http.server 8080

Open http://localhost:8080

## Deploy on Render
New → Static Site → connect this repo. Build command: empty. Publish directory: `.`
(or use the included `render.yaml` Blueprint)

## Structure
- `index.html` — the whole 3D world, tour script and UI
- `voice/` — narration clips (Ravi's lines and the receptionist)
- `img/` — avatar images for the dialog panel
