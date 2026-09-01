# Installation Guide

## Prerequisites

- Windows 10 or 11 (64-bit)
- ~500 MB free disk space
- Chrome, Edge, or Firefox
- Local admin rights are **not** required

## Steps

### 1. Download

Go to [Releases](https://github.com/S8619G/kyo-info-explorer/releases/latest) and download `Kyo-Info-Explorer.zip`.

### 2. Extract

Right-click the zip → **Extract All** → choose a destination. Recommended locations:

- `C:\Tools\Kyo Info Explorer`
- `%USERPROFILE%\Documents\Kyo Info Explorer`
- Anywhere else you have write access. Do **not** run it from inside the zip.

### 3. Run the one-time icon setup

Inside the extracted folder, double-click **`Setup Icon (run once).bat`**.

- A brief command window opens, creates the shortcut, and pauses for confirmation.
- You'll see a new `Kyo Info Explorer` shortcut in the folder with the red Kyocera icon.
- Press any key to close the setup window.

You only run this once per install.

### 4. Launch the app

Double-click the new **Kyo Info Explorer** shortcut. Your default browser opens at `http://127.0.0.1:5000` within a few seconds. No command window appears — the server runs invisibly in the background.

### 5. (Optional) Make the shortcut easily accessible

- **Desktop:** right-click the shortcut → **Send to → Desktop (create shortcut)**
- **Taskbar:** right-click the shortcut → **Pin to Taskbar**
- **Start menu:** copy the shortcut to `%APPDATA%\Microsoft\Windows\Start Menu\Programs`

## Stopping the app

Just close the browser tab. To fully stop the server:

- Open **Task Manager** → **Details** tab
- Find `node.exe` under the Kyo Info Explorer name and **End Task**
- Or simply log off / restart your PC

## Uninstalling

1. Delete the `Kyo Info Explorer` folder wherever you extracted it
2. To also remove uploaded manuals: delete `%LOCALAPPDATA%\KyoInfoExplorer\`

That's it. There is no installer, no registry footprint, no service.

## First-run warnings you might see

**"Windows protected your PC"** — click **More info** → **Run anyway**. Kyo Info Explorer is unsigned; this warning appears for any unsigned executable.

**Antivirus flagging node.exe** — add the folder to your antivirus exclusions. The bundled `node.exe` is the official Node.js runtime.

## Updating to a new version

1. Close the app (End the node.exe task if the browser tab already closed)
2. Download the new zip from Releases
3. Extract over the old folder — your `%LOCALAPPDATA%\KyoInfoExplorer\` data is untouched
4. Launch as before. The shortcut you created still works.

Uploaded manuals, database, and page images all survive updates.
