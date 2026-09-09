# Video Clipper — changelog

## 0.1.5 — 2026-09-09

Reverts the background color from the last release — that was a deliberate
test marker to confirm the updater fix, not a real design change.

## 0.1.4 — 2026-09-09

**Installer:** re-running the installer over an existing copy now offers an
**Update** option (selected automatically when it detects an older version
already installed) alongside Full install and Unzip.

Background color tweak, mostly to give this release something visible to
confirm the in-app updater actually applied it.

## 0.1.3 — 2026-09-09

Fixes the in-app updater itself: on a slower machine (or once the previous
release added the "will close and reopen" progress window), the app could
still be closing when the installer tried to replace its files, and the
update would silently do nothing — no error, just no update. The app now
closes immediately once the installer starts, so this can't happen.

## 0.1.2 — 2026-09-09

The update check now runs every time you open the app, not just once a day —
so if a new version is out, you'll see the prompt right when you launch
instead of having to open About and click **Check for updates** yourself.

## 0.1.1 — 2026-09-09

Adds the in-app updater. Video Clipper now checks for a new version when it
starts and offers a one-click update — download, verify, restart — instead of
you having to come back to the site. Check any time from **About → Check for
updates**.

Also adds a **Send feedback** option in the About dialog (bug / idea / comment),
so you can report something without leaving the app.

Note: this only takes effect from 0.1.1 onward — a 0.1.0 install has no updater
and needs a fresh download this once.

## 0.1.0 — 2026-09-08

First public beta.

A local, offline desktop video editor for Windows — no cloud upload, no
account. Bundles ffmpeg.

**Editing**
- Drag-and-drop a video (or a saved project). Trim with draggable handles or timecodes.
- Cut out middle sections; click a cut to adjust or delete it.
- Resolution, bitrate, and frame-rate control, with a live quality estimate and output-size readout.
- Optional cinematic motion blur when lowering the frame rate.

**Advanced mode**
- Sequence multiple clips, reorder by drag.
- Per-clip original-audio volume and mute regions; add and place new audio tracks.
- Approximate playback preview of the final result.

**Projects**
- Save and reopen your work as a `.vclip` project file (clips, trims, cuts, audio, export settings).
- Ribbon with Open / Save / Import / Export; an About dialog on the version chip.

Known limitations in this beta: the installer is unsigned, so Windows
SmartScreen shows an "unknown publisher" warning; there's no in-app updater
yet — check the site or this repo for new versions.
