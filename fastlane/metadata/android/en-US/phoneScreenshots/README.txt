# Phone screenshots

Place Vanta screenshots here before submitting to IzzyOnDroid.

Recommended: 2-5 screenshots showing:
1. Home screen with live tiles + weather
2. Apps drawer with search + recently used
3. Focus page (stopwatch/timers)
4. Live page (notifications + clock)
5. Settings (auto dark mode + auto refresh rate)

Filename convention: `en-US_1_home.png`, `en-US_2_apps.png`, etc.
Resolution: 1080x2400 (Pixel-sized) or 1080x1920 (16:9)

You can take screenshots via ADB:
```
adb -s 466871ba exec-out screencap -p > fastlane/metadata/android/en-US/phoneScreenshots/en-US_1_home.png
```
