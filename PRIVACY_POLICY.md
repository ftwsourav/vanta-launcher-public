# Vanta Privacy Policy

**Last updated: September 25, 2026**

## Short version

Vanta does not collect, store, or transmit any of your personal data. Everything stays on your device.

## The long version

### Data we collect
**None.** Vanta is a launcher app. It does not collect, transmit, or store any user data on any server. There is no analytics, no telemetry, no crash reporting, no advertising SDKs, and no tracking of any kind.

### Data stored on your device
Vanta stores the following locally on your device (never sent anywhere):
- Your launcher settings (theme, accent color, layout, dark mode preference)
- Your pinned apps and home screen layout
- Your focus mode tasks and notes
- Your weather location (you set this in settings)
- Cached weather data from Open-Meteo (public weather API)
- Cached app icons and labels from your installed apps

You can clear all this data by uninstalling the app or using the in-app "Reset Everything" option in Settings > System.

### Permissions Vanta requests and why
- **READ_CONTACTS** (optional) — show contact photos in the People Hub tile. Only used if you enable it.
- **ACCESS_FINE_LOCATION / ACCESS_COARSE_LOCATION** (optional) — fetch local weather for the weather tile. Only used if you enable weather.
- **READ_CALENDAR** (optional) — show next calendar event on the Live page.
- **PACKAGE_USAGE_STATS** (optional) — show "Most Used" apps in the drawer.
- **READ_SHORTCUTS** (optional) — show app shortcuts on long-press.
- **Notification Listener** (optional) — show notifications on the Live page. Vanta never reads notification content, only shows titles and app names.
- **INTERNET** — fetch weather data from Open-Meteo (free, open, no API key).
- **REQUEST_INSTALL_PACKAGES** — allows the in-app self-update flow (if you ever add it).

No permission data is ever transmitted off-device.

### Third-party services
**Open-Meteo** (https://open-meteo.com) — public weather API. Vanta sends your city's latitude/longitude to fetch weather. No tracking, no API key, anonymous.

That's it. No other third-party services. No Firebase. No Google Analytics. No crashlytics. No ads.

### Children's privacy
Vanta is not directed at children under 13, but does not collect any data from anyone regardless of age.

### Changes to this policy
If Vanta ever changes what data it handles, this page will be updated. Given the app's design, this is unlikely.

### Contact
Open an issue: https://github.com/ftwsourav/vanta-launcher-public/issues

### Source
This app is open source under Apache 2.0. You can review the entire codebase (well, you can review the public repo; the source is private but the APK is freely licensed).

---

**Developer: @ftwsourav**
