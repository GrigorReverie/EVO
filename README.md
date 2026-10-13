# EVO

Tools for the Evo member support team. Live at **https://grigorreverie.github.io/EVO/**

| Project | Folder | Link |
|---|---|---|
| EVO P2A | `EVO-P2A/` | https://grigorreverie.github.io/EVO/EVO-P2A/ |
| EVO P2A Rules (low AI) | `EVO-P2A-Rules/` | https://grigorreverie.github.io/EVO/EVO-P2A-Rules/ |

## EVO P2A
- **Sign in first.** Agents sign in with the name and password the admin gave them (Settings → Agents). The admin uses **Admin sign in** with a GitHub token that can write to the private `EVO-admin` repo.
- **AI runs inside the app.** Gemini is the default (free tier). Agents can connect ChatGPT or Claude with their own key; the admin can share a team key through the update file. The app picks a current model automatically.
- **Library.** The admin keeps the master in the private `EVO-admin` repo and pushes updates from the app (Settings → Library & updates). Agents get a notice, import the update file, and can send their own edits back for review.

## EVO P2A Rules (low AI)
Same app and same sign-in, library and updates as EVO P2A (it reads `EVO-P2A/agents.json` and `EVO-P2A/version.json`). Problem2Action matches the SOP from **trigger words**, name, tags and "When to use"; fills the reply and ticket templates from details found in the email; and lists the SOP's **info needed**, links and to-dos. No AI unless someone presses **✨ Ask AI**. Set trigger words and info needed in each SOP under **Matching (no AI)**, or use **Fill matching data** in SOPs.

## Files in this repo
- `EVO-P2A/index.html`: the app (built from the claude.ai version; no SOP content or internal links).
- `EVO-P2A/version.json`: which library update is newest. Written by the admin's **Push update** button.
- `EVO-P2A/agents.json`: the sign-in list. Only scrambled values; no names or passwords. Written by **Publish sign-in list**.

Don't edit `version.json` or `agents.json` by hand; the app manages them.
