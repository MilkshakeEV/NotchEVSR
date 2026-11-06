# Installing NotchEVSR

NotchEVSR turns the notch at the top of your MacBook screen into a small panel for music, your
calendar, apps, a file shelf, side-by-side views and temperatures. It needs an Apple
Silicon Mac (M1 or later) with macOS 14 Sonoma or newer.

## 1. Install
1. Open **NotchEVSR.dmg** (from the Download button on the releases page).
2. Drag **NotchEVSR** onto the **Applications** folder.
3. Eject the disk image.

## 2. Open it the first time
NotchEVSR isn't sold through the App Store, so macOS can't check it automatically. Expect a warning
the first time. On macOS 15 (Sequoia) and later, right-click → Open no longer gets around it.

1. Open **Applications** and double-click **NotchEVSR**.
2. macOS says it *cannot verify that NotchEVSR is free of malware*. Click **Done** (not "Move to Trash").
3. Open **System Settings → Privacy & Security** and scroll down to **Security**.
4. Next to "NotchEVSR was blocked to protect your Mac", click **Open Anyway**.
5. Click **Open Anyway** again and enter your Mac password.

You only do this once. Later versions arrive through **Check for Updates** inside the app.

**If the Open Anyway button doesn't appear**, or macOS says the app is "damaged", open
**Terminal** and run the following, then open NotchEVSR again:

```bash
xattr -dr com.apple.quarantine /Applications/NotchEVSR.app
```

This only removes the "downloaded from the internet" flag from NotchEVSR.

## 3. First run
A welcome window asks:

- **Which features you want.** Everything is on by default; untick what you don't need.
  Features you switch off never ask for permissions.
- **Whether NotchEVSR should start automatically** when you log in.
- **Permissions, only for the features you kept.** Each one can be skipped and turned on later:

| Permission | Used for |
|---|---|
| Calendars | Showing your Apple Calendar events (iCloud, Google, Exchange… whatever the Calendar app shows) |
| Reminders (optional) | Upcoming reminders under your events |
| Automation (rare) | Controlling Music/Spotify, only if the normal Now Playing route doesn't work |
| Login Items | Starting at login. macOS shows a "Background item added" notice; that's NotchEVSR |

After that, just **hover over the notch** to open the panel.

## Everyday tips
- The menu bar icon has Settings, Pause, Launch at Startup and Quit.
- If you hide the menu bar icon, press **⌃⌥⌘N**, or open NotchEVSR from Applications, to get back to Settings.
- Drag files onto the notch to park them on the **Shelf**, and drag them out later.
- The **Split View** page shows up to five modules at once (not the Shelf), for example music next to your calendar. Drag the
  little handle at its bottom edge down for a second row.

## Drop to Convert

The Shelf page has a Convert zone: drop images, documents or PDFs on it to get PDFs or images,
all on your Mac. It needs no permission. If you have Word, Excel, PowerPoint, Pages, Numbers or
Keynote, macOS asks once (Automation) the first time one of them is used for a conversion; that's
optional, and you can say no.

## Updating
Open **Settings → Updates** (or the menu bar icon → **Check for Updates…**) and click
**Check for Updates**. If a newer version exists you'll see it with its notes; click **Update**, then
**Install & Restart**. Updates come one version at a time, in order, and every download is checked
against its signature before it's installed. If something goes wrong, NotchEVSR puts the previous
version back by itself, and **Roll back to previous version** in Settings → Updates undoes an update.

NotchEVSR checks about once a day on its own (you can turn that off). It never interrupts you: a
small dot on the menu bar icon is the only sign that an update is waiting.

Keep NotchEVSR in your **Applications** folder: it can't update itself while it runs from the disk
image or the Downloads folder.

## Uninstalling
Use **NotchEVSR Settings → General → Uninstall NotchEVSR…**. It removes its startup item, settings,
saved data and the Shelf's own copies, then moves the app to the Trash. Your files are never touched.

## Privacy
No accounts, no tracking, nothing uploaded. The only network traffic is checking for and downloading
updates from GitHub, which sends nothing but the app's name and version.
