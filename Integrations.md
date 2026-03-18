---
layout: default
title: Integrations
---

Amazfish can connect to external fitness platforms to sync your activities.

## Strava

[Strava](https://www.strava.com/)

- Open **Amazfish**
- Go to **Settings → Strava**
- Click the **Login** button
- Authorize **Laufenheld** on the Strava webpage

---

## FitTrackee

[FitTrackee](https://github.com/SamR1/FitTrackee/)

To connect Amazfish with FitTrackee:

### 1. Create an application in FitTrackee

- Go to your profile → **Apps**
- Click **“Add an application”**

Fill in the form:

- **Application Name:** `Amazfish`
- **Application URL:** `http://127.0.0.1:1965/`
- **Redirect URL:** `http://127.0.0.1:1965/`
- **Scope:** select `workouts:write`

After submitting:

- You will see a **Client ID** and **Client Secret**
- ⚠️ Do **not close the page** — the secret will not be shown again

---

### 2. Configure Amazfish

- Open **Amazfish**
- Go to **Settings → FitTrackee**
- Fill in:
  - Your FitTrackee instance URL  
    (e.g. `https://fittrackee.de`)
  - **Client ID**
  - **Client Secret**
- Click **Login** and authorize the application