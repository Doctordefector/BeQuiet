# BeQuiet

A simple Windows 11 utility that "ducks" the volume of background apps.

Pick your priority apps (Discord, Telegram, etc.) and then they stay at full volume. Everything else gets quietly turned down. One click or hotkey to toggle.

## Features

- **Per-app volume control** via Windows Core Audio API
- **Multiple priority apps**  check as many as you want
- **Adjustable duck level**  slider from 5% to 90%, with quick presets (20/30/50/70)
- **Live re-ducking**  change the level while active, volumes update instantly
- **Global hotkey**  configurable, works even when the app is in the tray
- **System tray**  left-click to toggle, right-click for menu
- **Auto-duck new apps** — anything that starts playing audio while active gets ducked
- **Portable exe** 

## Usage

1. Launch `BeQuiet.exe`
2. Check the apps you want to keep at full volume
3. Set your duck level (how quiet everything else should be)
4. Click **ACTIVATE** or press your hotkey
5. Click again to deactivate and restore all volumes

Closing or minimizing the window sends it to the system tray. Right-click the tray icon → **Exit** to quit.


Uses the Windows Core Audio API (`IAudioSessionManager2`) via [NAudio](https://github.com/naudio/NAudio) to enumerate per-app audio sessions and control their volumes individually — the same mechanism the Windows Volume Mixer uses.

## License

MIT
