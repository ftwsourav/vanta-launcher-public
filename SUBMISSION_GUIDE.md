# How to publish Vanta on APKPure + Aptoide

Both are free, accept private-source APKs, no AI gate, no 30MB limit, no release-signing requirement. ~5 minutes each.

---

## A. APKPure (https://apkpure.com/submit-apk)

### Step 1 — Sign up
1. Go to https://apkpure.com/submit-apk
2. Click **Sign Up** (top right) if you don't have an account
3. Verify your email

### Step 2 — Upload APK
1. After signing in, go to the Developer Console
2. Click **Submit APK** or **Upload App**
3. Drag-drop `Vanta-v5.1.apk` (you have it at `C:\Users\Lab\Desktop\Brutalist Android launcher\Vanta-v5.1.apk`)
4. APKPure auto-extracts package name, version, icon from the APK

### Step 3 — Fill in app details
Use the metadata I prepared in `fastlane/metadata/android/en-US/`:

**App Name:** `Vanta` (from `title.txt`)
**Short Description** (80 chars max, from `short_description.txt`):
```
Brutalist Windows Phone Metro-inspired launcher with live tiles, 4-page pivot, auto dark mode, auto refresh rate.
```
**Full Description** (from `full_description.txt` — already written, ~3000 chars). Copy the entire content of `fastlane/metadata/android/en-US/full_description.txt`.

**Category:** `Personalization` (or `Tools`)
**Content Rating:** `Everyone`
**Developer:** `@ftwsourav`
**Website:** `https://github.com/ftwsourav/vanta-launcher-public`
**Privacy Policy:** `https://github.com/ftwsourav/vanta-launcher-public/blob/master/PRIVACY_POLICY.md`

### Step 4 — Upload screenshots + icon
- **Icon:** Use `logos/01_metro_tile_v_FINAL.svg` (or export to PNG). APKPure usually pulls the icon from the APK automatically.
- **Screenshots:** Optional but recommended. Take 3-5 via ADB:
  ```
  adb -s 466871ba exec-out screencap -p > fastlane/metadata/android/en-US/phoneScreenshots/en-US_1_home.png
  ```
  Then upload them. 1080×2400 px works.

### Step 5 — Submit
- Review → Submit
- APKPure reviews in ~1-3 business days
- You'll get an email when approved
- App appears at https://apkpure.com/vanta/com.xdlab.standard

---

## B. Aptoide (https://connect.aptoide.com/)

### Step 1 — Sign up
1. Go to https://connect.aptoide.com/register
2. Create a developer account (free)
3. Verify email

### Step 2 — Create a Store (optional but recommended)
Aptoide lets you have your own "store" — think of it as a mini app store branded to you.
1. In the Connect dashboard, click **Create Store**
2. Name it `ftwsourav` or `Vanta Apps`
3. Pick a theme color (use `#FF6F00` — the Vanta accent)

### Step 3 — Add your app
1. Click **Add App** in the dashboard
2. Upload `Vanta-v5.1.apk`
3. Aptoide parses the package name + version automatically

### Step 4 — Fill app details (same as APKPure)
Use the same metadata from `fastlane/metadata/android/en-US/`:
- **App Name:** `Vanta`
- **Short Description:** (from short_description.txt)
- **Full Description:** (from full_description.txt)
- **Category:** `Personalization` → `Launcher`
- **Developer:** `@ftwsourav`
- **Website / Privacy Policy:** same URLs as APKPure
- **Age rating:** All ages

### Step 5 — Upload screenshots + feature graphic
- **Feature Graphic:** 1024×500 px. I created `logos/hero_banner.svg` — export to PNG 1024×500, or use any image editor to convert.
- **Screenshots:** same as APKPure

### Step 6 — Submit
- Click **Submit for Review**
- Aptoide reviews in ~1-2 business days
- Once approved, Vanta appears at https://vanta-apps.en.aptoide.com (or similar, based on your store name)

---

## Quick file reference

| File | Use |
|---|---|
| `Vanta-v5.1.apk` | The APK to upload (60 MB — both stores accept this) |
| `fastlane/metadata/android/en-US/title.txt` | App name: "Vanta" |
| `fastlane/metadata/android/en-US/short_description.txt` | 80-char description |
| `fastlane/metadata/android/en-US/full_description.txt` | Long description |
| `fastlane/metadata/android/en-US/changelogs/51.txt` | Changelog (v5.1) |
| `PRIVACY_POLICY.md` | Privacy policy URL |
| `logos/01_metro_tile_v_FINAL.svg` | App icon |
| `logos/hero_banner.svg` | Feature graphic (export to 1024×500 PNG) |

## If they ask questions

- **"Is the source open?"** → "Source is private; the APK is freely distributable. The public repo has README, license, fastlane metadata, and privacy policy."
- **"Does it contain trackers?"** → "No. No Firebase, no Analytics, no ads. The privacy policy confirms zero tracking."
- **"What permissions and why?"** → See the privacy policy — all permissions are optional and user-controlled.
- **"How do users update?"** → "I publish new APKs to GitHub releases; users re-download. (Or Aptoide/APKPure handle updates automatically once a new version is uploaded to their platform.)"

## After approval

You'll get store URLs like:
- APKPure: `https://apkpure.com/vanta/com.xdlab.standard`
- Aptoide: `https://<your-store>.en.aptoide.com/vanta`

Add these to your README's download section so users have options:
- GitHub Releases (direct APK)
- APKPure
- Aptoide

Update the README by adding the store links once you have them. I can do that for you when you send me the URLs.

---

## Tips

- **Both stores auto-update from your uploads.** When you publish v5.2, just upload the new APK to each store and users get the update automatically.
- **APKPure has a bigger audience in Asia/Europe.** Aptoide is big in Latin America and Europe. Both complement GitHub (which is more developer-focused).
- **No fees either way.** Both are free for developers.
- **You keep 100% of control.** Unlike Play Store, neither requires you to use their billing or sign exclusivity.

Good luck! Tell me when you've submitted and I'll help with any follow-up, or send me the store URLs and I'll update the README.
