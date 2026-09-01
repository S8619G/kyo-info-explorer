# Troubleshooting

## "Windows protected your PC" popup on first launch

Click **More info** then **Run anyway**. This is normal for unsigned local applications. Kyo Info Explorer is not signed with a code-signing certificate; the popup is Windows SmartScreen warning about any unsigned executable.

## Antivirus flags node.exe

The bundled `node.exe` is the standard Node.js runtime from nodejs.org (bundled so no separate install is needed). If your antivirus is aggressive, add the Kyo Info Explorer folder to its exclusions list.

## Port 5000 is already in use

Close whatever else is using it (another Kyo Info Explorer window, or a local dev server). The launcher tries to free the port automatically, but sometimes a stuck process needs manual cleanup via Task Manager.

## Browser opens but nothing loads

Wait 5–10 more seconds and refresh. First launch is slower because the database is being seeded from the shipped `seed.db`.

## PDF upload fails with "failed to fetch"

1. Check `%LOCALAPPDATA%\KyoInfoExplorer\server.log` for the last few lines — this usually shows the crash cause
2. Verify the file is under 150 MB
3. Try restarting the app and uploading again
4. If the launcher is running via the icon (hidden mode) and the server crashed, a visible cmd window should have popped up with the exit code — screenshot and share

## Large PDF upload takes forever

Manuals of 500+ pages can take 60–180 seconds to process (extract text, chunk, embed, and render page images). This is normal. The Upload button will spin the entire time. Look at `server.log` for progress.

## Shortcut icon doesn't appear

Run `Setup Icon (run once).bat` from the app folder. If that fails, you can always launch the app with `Start Kyo Info Explorer.bat` — same result, just with a visible command window.

## Print button prints only one page

Update to v0.9.12 or newer — earlier versions could only print the current page. Newer versions have a Range option in the Print popover.

## Getting the log file to report a bug

Full log path: `%LOCALAPPDATA%\KyoInfoExplorer\server.log`

Open **File Explorer**, paste that path in the address bar, and open with Notepad. The last chunk (bottom of the file) will contain the most recent activity.

## Fresh start / wipe database

1. Close the app (End Task in Task Manager if the browser tab already closed)
2. Delete the folder `%LOCALAPPDATA%\KyoInfoExplorer\`
3. Launch the app again — it'll recreate everything from the shipped seed database

Your uploaded manuals will be gone but the two preloaded TASKalfa guides will return.
