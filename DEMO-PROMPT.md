# Demo Generator Prompt

Copy and paste this into any Claude Code project to generate an interactive sales demo.

---

```
Build me an interactive sales demo for this project as a single self-contained HTML file called `demo.html`. The demo is for pitching this product/flow to prospective clients.

Requirements:

1. **Analyze the project first** — read the main source files to understand the core user-facing flow, key features, and any escalation/notification/status logic.

2. **Self-contained** — single HTML file, no server, no dependencies beyond CDN links (Tailwind CDN, Google Fonts). Must work by just opening the file in a browser.

3. **Visually match the real product** — use the same styling, color palette, card layouts, badges, and typography from the actual dashboard/UI. Copy the exact Tailwind classes and design patterns.

4. **Use fake data only** — 3-4 realistic but fictional examples (fake client names, fake team member names). No real tokens, IDs, or sensitive data.

5. **Interactive time/state controls** at the top:
   - Play/Pause button that auto-advances the simulation (~3 seconds per step)
   - Manual step buttons (e.g. "+1 step", "+4 steps", skip to key moments)
   - Reset button to restart the demo
   - Display showing current simulated time/state

6. **Two-panel layout**:
   - **Left (main)**: The product dashboard/UI showing live status updates as the simulation runs
   - **Right (sidebar)**: A feed/log showing the actions the product takes (notifications sent, status changes, alerts triggered) — styled to match where these would actually appear (e.g. Slack-style messages, email previews, log entries)

7. **Show the full lifecycle** — the simulation should walk through the complete flow from start to finish, hitting every key state/threshold. Include at least one "recovery" or "success" scenario (e.g. a user responds and the status resets to good).

8. **Smooth animations** — slide-in effects for new feed items, smooth transitions for status badge changes.

After building demo.html, copy it as `index.html` into a subfolder of ~/Desktop/thinkflow-demos/ named after this project (e.g. thinkflow-demos/project-name/index.html), then commit and push to the thinkflow-demos repo so it goes live on GitHub Pages.
```
