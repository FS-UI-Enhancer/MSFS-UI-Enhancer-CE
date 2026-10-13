# UI Enhancer Community Edition for Microsoft Flight Simulator 2024

UI Enhancer Community Edition is the free edition of UI Enhancer. It adds **favourite aircraft** and an **aircraft setup panel** to the aircraft picker, **one screen corner** with an in-flight panel, a **landing rate notification** after each touchdown and a tidier **in-flight toolbar**. It's designed to fit in with the simulator's own look.

You choose and configure everything in the **UI Enhancer Manager** app, which also installs, updates and removes UI Enhancer.

> **Status:** early release. Aircraft favourites are in daily use; the in-flight panels are newer and still being tested.

---

## Features

### Favourite aircraft

Heart the aircraft you fly most and get to them quickly. Every aircraft in the aircraft picker has a heart: click it to add that aircraft to your favourites, or take it off. A Favourites tab shows just your favourites, and the picker opens on it next time if that's where you left it. Your favourites are kept between sessions in your simulator profile's save.

While favourite aircraft are on, the picker's Marketplace tab is hidden: the tab row only has room for so many tabs, and the Favourites tab would push Marketplace off the end. The Marketplace is still on the home screen.

**Favourite aircraft menu:** a Favourite aircraft button under the aircraft on the Free Flight screen, so you can fly one of your favourites without opening the aircraft picker.

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

The bottom-right corner is kept for UI Enhancer's notifications. They pop out by that corner when something happens, then fade away; click the triangle in the corner to see this flight's notifications again. Choose which ones you want on the app's **In flight** page.

- **Landing rate:** after each touchdown, your landing rate with a rating (butter to very hard), the G-load, speeds, wind, slip and any bounces.

### Diamond toolbar tab

The in-flight toolbar stays out of the way until you want it. Instead of popping up whenever the mouse goes near the top of the screen, it opens from a small diamond that fades in at the top centre; click it to open the toolbar, and click it again (or move off the toolbar) to close it. The toolbar buttons are shown as separate tiles.

Turn on **Hide toolbar tooltips** in the same panel to stop the name labels popping up under the toolbar buttons. It works with or without the diamond tab.

### UI Enhancer Pro

UI Enhancer Pro has everything in Community Edition, plus:

- **All three screen corners**, with **SimBrief** plans in Flight progress (navlog, fuel & payload, weather and the full OFP) and **BeyondATC** in the ATC panel.
- **More aircraft picker features:** list layouts, the sort menu and a steadier list.
- **Free Flight screen:** better airport picking (recent routes, favourite airports and grouped start positions).
- **Start-up and banner options.**
- **Scratchpad** in Utilities: ATIS, QNH, squawk, a frequency and notes, kept until you clear them.

In the app, Pro features are marked **PRO**.

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
   - Click **Install**, with the simulator closed: it only reads add-ons when it starts.
4. **Start the simulator.**

## Changing settings

Open `UIEnhancerManager.exe` and pick a page on the left. To place your corner, go to **In flight**: it shows a picture of the flight screen. Click a corner and choose what goes there; click anything on the picture to set it up.

When you change something, a bar appears at the bottom: click **Apply**, then start the simulator to see the changes. Close the simulator before applying: it only reads add-ons when it starts. **Reset to recommended** at the top of each page puts that page back to the recommended settings.

## After a simulator update

UI Enhancer carries copies of a few of the simulator's menu components. After a simulator update, open the app with the simulator closed and it rebuilds them from the new versions; if **Home** says _The simulator was updated_, click **Apply again**. Your settings and favourites are kept.

If parts of UI Enhancer stop working after a big simulator update, check here for a new release. The app also tells you when one is available.

## Simulator settings backups

The app keeps copies of the simulator's settings file (`UserCfg.opt`, which holds your graphics, display and other options), so a settings reset can be spotted and undone. It checks the file when the app starts and whenever the simulator closes, and keeps the last 20 versions in `%APPDATA%\UIEnhancer\usercfg`.

If any settings changed since the last backup, **Home** and the **Installation** page list each one, with its old and new value. If you changed them yourself, click **Dismiss**. Otherwise, close the simulator and click **Undo** next to a setting to put just that one back, or **Restore all** for the whole file; your current settings file is backed up first, so this can be undone. The **Installation** page also lists every backup, each with **Restore**. Settings the simulator changes by itself every session, such as the window position, aren't reported.

## Uninstalling

1. Close the simulator and open the app.
2. On the **Installation** page, click **Remove**. This deletes UI Enhancer's folder from Community; your favourites stay saved.
3. Delete the folder you extracted the app to.
4. Optional: delete `%APPDATA%\UIEnhancer` to remove the app's settings, log and simulator settings backups.

---

## How it works

UI Enhancer installs as a Community folder add-on (`ui-enhancer`). It carries its own copies of three of the simulator's menu components, each of which starts UI Enhancer's scripts. **The simulator's own files aren't changed.** The only exception is the simulator's settings file, and only when you click **Restore previous settings** (see [Simulator settings backups](#simulator-settings-backups)).

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
