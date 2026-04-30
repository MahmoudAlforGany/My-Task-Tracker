Mahmoud AlforGany Task Tracker — /data/ Folder
================================================

This folder holds a single shared data file used by the app to persist
your tasks, status/priority/department lists, and tips across browsers
and devices.

  data/tasks.json   <- the file the app reads / writes

How to set it up (cross-browser sync)
--------------------------------------

1. Open the app (index.html) in Chrome, Edge or Brave.
2. Click the green/grey "Sync" pill in the top-right header (or open
   Settings → Sync).
3. Press "Connect Data File".
4. In the OS save dialog that appears, navigate INTO this /data/ folder
   and pick (or create) the file named  tasks.json  then click Save.
5. The app remembers the file. Every change is now auto-written to it.

Repeat steps 1-4 in any other browser or device that opens this folder
(e.g., laptop Chrome + desktop Edge). They all share the same file
through OneDrive / GitHub / Dropbox sync, so your tasks stay in sync.

After making changes in another browser, click "Reload from File"
in Settings → Sync (or the small refresh action) to pull the latest.

Notes
-----
- File System Access API is required (Chrome / Edge / Brave / Opera).
  Firefox & Safari can still read data/tasks.json on initial load when
  served via http(s), but cannot write back automatically.
- For GitHub Pages: place tasks.json next to index.html in /data/ and
  it will load automatically on every visit (read-only without
  connecting). To push updates, commit the file like any other change.
- Format: standard JSON with this shape:
    {
      "version": 1,
      "savedAt": "ISO timestamp",
      "tasks":  [ ... ],
      "config": { "statusList": [...], "priorityList": [...], "departmentList": [...] },
      "tips":   [ { "cat": "...", "text": "..." } ]
    }
