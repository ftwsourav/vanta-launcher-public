# How to submit Vanta to IzzyOnDroid (F-Droid community repo)

IzzyOnDroid is a curated F-Droid repository that hosts pre-built APKs. It's free, popular with the FOSS community, and accepts apps with proper licenses even if the source is private.

## Step 1 — Already done
I've prepared in this repo:
- `LICENSE` — Apache 2.0 (required)
- `fastlane/metadata/android/en-US/` — store listing (title, description, changelog)
- `fdroid/metadata.yml` — F-Droid metadata template
- `PRIVACY_POLICY.md` — privacy policy

## Step 2 — Submit to IzzyOnDroid

1. Go to: https://gitlab.com/IzzyOnDroid/repo/-/issues/new
2. Sign in with a GitLab account (free to create)
3. Fill in the issue with this template:

### Issue title:
`[Submission] Vanta — Brutalist Metro launcher`

### Issue body (copy/paste this):

```
**App name:** Vanta
**Package name:** com.xdlab.standard
**Version:** 5.1 (versionCode 51)
**License:** Apache-2.0
**Source:** https://github.com/ftwsourav/vanta-launcher-public (APK + metadata; source code is private but the APK is freely licensed)
**Latest APK:** https://github.com/ftwsourav/vanta-launcher-public/releases/download/v5.1/Vanta-v5.1.apk
**Releases page:** https://github.com/ftwsourav/vanta-launcher-public/releases
**Privacy policy:** https://github.com/ftwsourav/vanta-launcher-public/blob/master/PRIVACY_POLICY.md
**Description:** Brutalist Windows Phone Metro-inspired Android launcher with live tiles, 4-page pivot, auto dark mode, auto refresh rate, tablet support. Built with Kotlin + Jetpack Compose. No tracking, no ads, no cloud.

**Author:** @ftwsourav
**Categories:** Phone & SMS, System, Personalization

**Why I want this on IzzyOnDroid:** Vanta is a privacy-respecting launcher with zero telemetry. The FOSS community would appreciate a clean, productivity-focused launcher with the Lumia Metro aesthetic.
```

4. Attach the APK file (download it from the GitHub release first, then upload to the issue)
5. Submit the issue

## Step 3 — Wait for review

IzzyOnDroid reviews submissions manually. Typical wait: 1-7 days. They'll respond in the issue with questions or accept it.

They may ask:
- "Is the source open?" — answer: "Source is private, but the APK is Apache-2.0 licensed and freely distributable. The public repo has the README, license, fastlane metadata, and privacy policy."
- "What tracking libraries are included?" — answer: "None. No Firebase, no Analytics, no ads."
- "Anti-features?" — answer: "None. The app uses Open-Meteo (public weather API, no key)."

## Step 4 — After approval

Once approved, Vanta will appear in the IzzyOnDroid repo. Users can install it via:
- F-Droid app → add IzzyOnDroid repo (https://apt.izzysoft.de/fdroid/repo)
- Or directly from https://apt.izzysoft.de/fdroid/index/apk/com.xdlab.standard

## Notes
- IzzyOnDroid auto-updates from your GitHub releases if you keep the same filename pattern. I've set up `fdroid/metadata.yml` to scrape the latest tag automatically.
- Future releases: just publish a new GitHub release with `Vanta-vX.Y.apk` and IzzyOnDroid will pick it up within ~24 hours (if they accept auto-update mode).
