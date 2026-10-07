# SetMachinePlateInfo

FreeCAD macro to fill in the texts of the machine plates, update the CAM job and export the gcode for the engraving machine.

Requires FreeCAD 1.1 or newer.

## Installing

Find your FreeCAD macro folder: in FreeCAD, open **Macro → Macros...**. The folder is shown at the bottom of the dialog ("User macros location").

### Option 1: Download the file (simplest)

1. Open `SetMachinePlateInfo.FCMacro` on the GitHub page of this repository.
2. Click the **Download raw file** button.
3. Put the file in the macro folder, replacing the old version.

To update, repeat these steps.

### Option 2: Using git

Run these commands once, inside the macro folder (this also works when the folder already contains other macros):

```
git init
git remote add origin <repository URL>
git pull origin main
```

To update to the newest version later:

```
git pull origin main
```

## Using the macro

1. Open the machine plate document (it must contain the CAM job called `Job`).
2. Run the macro: **Macro → Macros...**, select `SetMachinePlateInfo.FCMacro` and click **Execute**.
3. Fill in the texts on the **Engraving** tab and uncheck the plates you do not want to engrave.
4. Click **Generate** and choose where to save the gcode.

Which plates are enabled is stored in the CAM job. **Save the document** to keep that, and the texts, for next time.

## When something goes wrong

- When an error occurs, an error window appears. Click **Copy Error Report** and paste the report in a message to Arwin.
- If the result is wrong but there was no error (for example wrong positions or missing text), open the **Config** tab, click **Copy Diagnostics** and send that.
- Everything the macro does is written to a log file, `SetMachinePlateInfo.log`, in the FreeCAD user folder. The **Open Log Folder** button on the Config tab opens that folder.
- The version of the macro is shown in the title of the window. Mention it when reporting a problem.
