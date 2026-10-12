# UI Enhancer Community Edition for Microsoft Flight Simulator 2024

UI Enhancer Community Edition is the free edition of [UI Enhancer](https://github.com/robertmacnair/MSFS-UI-Enhancer). It adds **favourite aircraft** and an **aircraft setup panel** to the aircraft picker, **one screen corner** with an in-flight panel and a **landing rate notification** after each touchdown. It's designed to fit in with the simulator's own look.

You choose and configure everything in the **UI Enhancer Manager** app, which also installs, updates and removes UI Enhancer.

> **Status:** early release. Aircraft favourites are in daily use; the in-flight panels are newer and still being tested.

---

## Features

### Aircraft favourites

A Favourites tab and a heart on every aircraft tile in the aircraft picker. Click a heart to add or remove that aircraft. Your favourites are kept between sessions in your simulator profile's save.

### Aircraft setup panel

Variant, livery and identification right in the aircraft picker. The left panel shows the aircraft's setup instead of its statistics: variant and livery dropdowns (with a livery filter, preview and favourite liveries) and identification, plus buttons for Fuel & Payload and Mass & Balance.

### One screen corner

Place one of these in a corner of the screen. Nothing shows until you move the mouse into that corner; click the triangle that appears to open it.

- **Flight progress:** a route progress banner and a menu with your flight's details, using the departure and arrival you set on the world map.
- **Utilities:** a stack of small tools; each icon opens its tool beside the stack.
  - **Sim rate:** see and change the simulation rate (¼× to 16×), with a reminder badge while it isn't 1×.
  - **Active pause:** one click turns it on or off.
  - **Time of day:** Dawn, Morning, Noon, Sunset, Dusk and Night presets that follow the sun where you are, and back to live time.
  - **Timers:** a stopwatch and a countdown that run on the sim's clock.
- **ATC:** the simulator's ATC in a compact panel. It shows the conversation, your replies as buttons and COM1 with a swap button. When ATC calls you, the panel pops out so you can reply.

### Notifications

**Landing rate:** after each touchdown, your landing rate fades in by the bottom-right corner, with a rating, the G-load, speeds, wind, slip and any bounces. Click the triangle in that corner to see this flight's landings again.

### UI Enhancer Pro

[UI Enhancer Pro](https://github.com/robertmacnair/MSFS-UI-Enhancer) has everything in Community Edition, plus:

- **All three screen corners**, with **SimBrief** plans in Flight progress (navlog, fuel & payload, weather and the full OFP) and **BeyondATC** in the ATC panel.
- **More aircraft picker features:** list layouts, the sort menu and a steadier list.
- **Free Flight screen:** better airport picking and the Favourite aircraft menu.
- **Start-up and banner options.**
- **Scratchpad** in Utilities: ATIS, QNH, squawk, a frequency and notes, kept until you clear them.
- The **diamond toolbar tab**.

The app shows Pro features with a **PRO** tag.

---

## Requirements

- Microsoft Flight Simulator 2024, **Microsoft Store or Steam**.
- Windows 10 or 11.
- Microsoft Edge **WebView2 Runtime**. It's already part of Windows 11 and almost every up-to-date Windows 10 PC; the app tells you if it's missing.

## Installing

1. **Download** the latest `UIEnhancer-Community-<version>.zip` from the [Releases](../../releases) page and **extract** it to a folder of your choice, for example `Documents\UIEnhancer`. Don't extract it into the Community folder; the app installs UI Enhancer there itself.
2. **Run `UIEnhancerManager.exe`.**
   If Windows shows _"Windows protected your PC"_, click **More info**, then **Run anyway**.
3. A short **setup** guides you through the rest:
   - The app **finds the simulator and its Community folder automatically**. If it can't, click **Browse** and choose them.
   - Choose **Recommended** or **Everything off** as a starting point.
   - Click **Install**. If the simulator is running, UI Enhancer installs itself as soon as you close it.
4. **Start the simulator.**

## Changing settings

Open `UIEnhancerManager.exe` and pick a page on the left. To place your corner, go to **In flight → Screen corners** and choose a feature for one corner.

When you change something, a bar appears at the bottom: click **Apply**, then start the simulator to see the changes. If the simulator is running, click **Apply when it closes** and UI Enhancer applies them as soon as you close it.

## After a simulator update

UI Enhancer carries copies of a few of the simulator's menu components. After a simulator update, open the app with the simulator closed and it rebuilds them from the new versions; if **Home** says _The simulator was updated_, click **Apply again**. Your settings and favourites are kept.

If parts of UI Enhancer stop working after a big simulator update, check here for a new release. The app also tells you when one is available.

## Uninstalling

1. Close the simulator and open the app.
2. On the **Installation** page, click **Remove**. This deletes UI Enhancer's folder from Community; your favourites stay saved.
3. Delete the folder you extracted the app to.
4. Optional: delete `%APPDATA%\UIEnhancer` to remove the app's settings and log.

---

## How it works

UI Enhancer installs as a Community folder add-on (`ui-enhancer`). It carries its own copies of three of the simulator's menu components, each of which starts UI Enhancer's scripts. **The simulator's own files aren't changed.**

- **Your data:** favourites live in your simulator profile's own save, so they follow your profile.
- **Privacy:** everything runs on your PC. The app checks this page for new releases; nothing else is sent anywhere.

## Troubleshooting

- **"WebView2 Runtime isn't installed":** click _Yes_ in that message to open Microsoft's download page, install it, and start the app again.
- **A feature isn't showing in the simulator:** make sure you restarted the simulator after applying, and that **Home** says _Installed and up to date_.
- **Another add-on changes the same menus:** the **Installation** page lists any add-on that replaces the same components. Only one of them can work; remove one.
- **Reporting a problem:** on **Home** (or **About & support**), click **Copy diagnostics** and paste the result into a new issue on the [Issues](../../issues) page, along with what you did and what you expected.

---

## Disclaimer

UI Enhancer is an unofficial add-on and is not affiliated with or endorsed by Microsoft or Asobo Studio. Use it at your own risk; **Remove** in the app takes it out of the simulator.

## Credits

- [Roboto](https://fonts.google.com/specimen/Roboto) font by Google, under the Apache License 2.0.

## Licence

UI Enhancer Community Edition is free to use. It may not be copied, modified, redistributed or sold, in whole or in part, without permission. All rights reserved. See [LICENSE](LICENSE).
