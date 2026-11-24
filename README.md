# FlipClock Screensaver

A minimalist split-flap digital clock screensaver for Windows 10 and Windows 11.

## Welcome

Thank you for trying FlipClock Screensaver! This application turns your display into a clean, animated clock while your computer is idle.

## What's included

The distribution folder should contain these three files:

```text
FlipClockScreensaver-v1.0/
├── FlipClockScreensaver.scr
├── Install-Screensaver.ps1
└── README.md
```

- **FlipClockScreensaver.scr** — the screensaver application.
- **Install-Screensaver.ps1** — the installer and uninstaller.
- **README.md** — these user instructions.

## System requirements

- Windows 10 or Windows 11 (64-bit).
- Administrator permission to install or uninstall the screensaver.
- The three package files kept together before installation.

## Installation

1. Download and extract the FlipClock Screensaver package.
2. Make sure `FlipClockScreensaver.scr` and `Install-Screensaver.ps1` are in the same folder.
3. Right-click `Install-Screensaver.ps1` and select **Run with PowerShell**.
4. In the installer menu, choose **1 — Install**.
5. If Windows displays a User Account Control prompt, review it and select **Yes** to allow installation.
6. When installation finishes, Windows Screen Saver Settings should open.
7. Select **FlipClockScreensaver** from the Screen saver list if it is not already selected.
8. Choose the desired wait time, then select **Apply**.

> The installer places the screensaver in the Windows system screensaver folder. Administrator permission is required for this operation.

## Configure FlipClock

1. Open Windows Screen Saver Settings:
   - Press `Windows + R`.
   - Enter `control desk.cpl,,@screensaver`.
   - Press Enter.
2. Select **FlipClockScreensaver**.
3. Click **Settings...** to open the FlipClock options.
4. Adjust the available clock preferences.
5. Click **Save** to apply your preferences.

Available options depend on the version of FlipClock included in your package. They may include:

- 12-hour or 24-hour time format.
- Show or hide seconds.
- Show or hide AM/PM.
- Show or hide the date.
- Clock size.
- Display brightness.
- Flip animation duration.
- Multiple-monitor display.

## Preview and use

- In Windows Screen Saver Settings, select **Preview** to see the screensaver.
- To test it directly, open PowerShell and run:

  ```powershell
  & "$env:WINDIR\System32\FlipClockScreensaver.scr" /s
  ```

- Move the mouse, click, or press a key to exit the full-screen screensaver.

## Uninstall

1. Open the folder containing `Install-Screensaver.ps1`.
2. Right-click the script and select **Run with PowerShell**.
3. Choose **2 — Uninstall**.
4. Approve the User Account Control prompt.
5. The installer removes the installed screensaver file.

Uninstalling preserves your personal FlipClock preferences. If you want to remove those preferences too, delete this folder after uninstalling:

```text
%LOCALAPPDATA%\FlipClockScreensaver
```

## Troubleshooting

### FlipClock does not appear in the Screen Saver list

- Confirm installation completed successfully.
- Check that `C:\Windows\System32\FlipClockScreensaver.scr` exists.
- Close and reopen Windows Screen Saver Settings.
- If your organization manages screen saver settings, contact your administrator.

### The Settings button does not open the FlipClock options

First check that FlipClock is selected in the Screen Saver list. You can also test the configuration window directly from PowerShell:

```powershell
& "$env:WINDIR\System32\FlipClockScreensaver.scr" /c
```

If the settings window still does not appear, contact the person who supplied this package and include any error message.

### Windows blocks the PowerShell installer

Only run the installer if you trust the source of the package. You can open PowerShell in the extracted package folder and run:

```powershell
powershell.exe -NoProfile -ExecutionPolicy Bypass -File .\Install-Screensaver.ps1
```

Windows may still ask you to approve administrator access.

### The screensaver does not start

- Confirm FlipClock is selected in Windows Screen Saver Settings.
- Check that the wait time is greater than zero.
- Try the **Preview** button.
- Check whether another application or organization policy prevents screensavers from running.

## Privacy

FlipClock stores its display preferences locally on your Windows computer. The standard settings location is:

```text
%LOCALAPPDATA%\FlipClockScreensaver
```

The installer does not need your email address or an online account.

## Support

For help, contact the person or organization that provided this FlipClock Screensaver package. Include your Windows version and a description or screenshot of the problem.

---

**FlipClock Screensaver**  
Thank you for using FlipClock!
