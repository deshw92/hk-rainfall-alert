# 🌧 HK Rainfall Alert

A lightweight web app that monitors **real-time Hong Kong rainfall** using the HKO Open Data API and alerts you when rain exceeds your threshold.

🌐 **Live App:** https://hans-tsang.github.io/hk-rainfall-alert/

## Features

- 📍 Auto-detects your GPS location or manually select from 18 HK districts
- 🌧 Real-time rainfall display per district with visual bar chart
- 🔔 Browser push notifications when rain exceeds your threshold
- 📧 Email alert via `mailto:` (opens your mail client)
- ⚙️ Notification preferences — adjustable rain threshold (0–20 mm), quiet hours (11 pm – 7 am), alert sound toggle
- 📱 iPhone Shortcut guide — set up an alarm that wakes you when it's raining
- 🔄 Auto-refreshes every 6 minutes
- 🌤 Today's weather outlook from HKO forecast API
- 💾 All preferences saved to localStorage
- 🌙 Dark theme (blue/slate palette), mobile-first design

## Data Source

- **Rainfall API:** `https://data.weather.gov.hk/weatherAPI/opendata/weather.php?dataType=rhrread&lang=en`
- **Forecast API:** `https://data.weather.gov.hk/weatherAPI/opendata/weather.php?dataType=flw&lang=en`
- HKO JSON APIs — updated every 15 minutes, no CORS issues
- Docs: [HKO Open Data](https://www.hko.gov.hk/en/abouthko/opendata_intro.htm)

## iPhone Shortcut — Rain Alarm

Want to get woken up by an alarm when it's raining? The app includes a step-by-step guide for building an **Apple Shortcut** that:

1. Calls the HKO rainfall API directly from your iPhone
2. Checks if rainfall in your district exceeds a threshold
3. Creates an alarm set to ring in 1 minute with rain details as the label

👉 **[Open the iPhone Shortcut Guide](shortcut-guide.html)**

Set up a 15-minute automation to run the shortcut automatically during your morning hours — no server needed.

## Notification Methods

| Method | How it works | Requires |
|---|---|---|
| Browser Push | Native notification popup | Click "Enable" in app + allow in browser |
| Email (mailto) | Opens your mail client with rain info | Enter email in app |
| Alert Sound | Two-tone audio alert in browser | Enable in Notification Preferences |
| iPhone Alarm | Creates a Clock alarm via Shortcut | Set up the Shortcut (see guide) |

## Local Development

Just open `index.html` in a browser — no build step, no dependencies, no backend.

```
open index.html
```

All files are static HTML/CSS/JS, ready for GitHub Pages.
