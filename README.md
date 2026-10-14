# EVO

Tools for the Evo member support team. Live at **https://grigorreverie.github.io/EVO/**

| Project | Folder | Link |
|---|---|---|
| EVO P2A | `EVO-P2A/` | https://grigorreverie.github.io/EVO/EVO-P2A/ |

## EVO P2A
- **Sign in first.** Agents sign in with the name and password the admin gave them (Settings → Agents). The admin uses **Admin sign in** with a GitHub token that can write to the private `EVO-admin` repo.
- **Rules first, AI on demand.** Problem2Action matches the SOP from **trigger words**, name, tags and "When to use"; fills the reply and ticket templates from details found in the email; and lists the SOP's **info needed**, links and to-dos. AI runs only when someone presses **✨ Ask AI**. Set trigger words and info needed in each SOP under **Matching (no AI)**, or use **Fill matching data** in SOPs.
- **AI runs inside the app.** Gemini is the default (free tier). Agents can connect ChatGPT or Claude with their own key; the admin can share a team key through the update file. The app picks a current model automatically.
- **Library.** The admin keeps the master in the private `EVO-admin` repo and pushes updates from the app (Settings → Library & updates). Each push also saves a dated copy in `Library Version History`.
- **Vault.** Each push saves the latest library, encrypted, as `EVO-P2A/vault.json`. Agents tap **Get latest from the Vault**; their sign-in password unlocks it. Nobody else can read it.

## Files in this repo
- `EVO-P2A/index.html`: the app (built from the claude.ai version; no SOP content or internal links).
- `EVO-P2A/version.json`: which library update is newest. Written by the admin's **Push update** button.
- `EVO-P2A/vault.json`: the latest library, encrypted. Written by **Push update**.
- `EVO-P2A/agents.json`: the sign-in list. Only scrambled values; no names or passwords. Written by **Publish sign-in list**.
- `EVO-P2A-Rules/index.html`: forwards old links to `EVO-P2A/`.

Don't edit `version.json` or `agents.json` by hand; the app manages them.
