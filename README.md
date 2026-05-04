# Neverness to Everness (NTE) - FPS Unlock by modifying GameUserSettings.

## Instructions
1. Press `Win + R`, paste the following, and hit Enter: `%LocalAppData%\HT\Saved_Global\Config\Windows`
2. Right-click `GameUserSettings.ini` and open it with any text editor (Notepad, Notepad++).
3. Scroll to the very bottom and add a new line. Paste this:
```
[/Script/HTGame.HTGameUserSettings]
bUseVSync=False
FrameRateLimit=200.000000
```
(Change `200.000000` to your desired value. Do not use `0.000000` or values below `30.000000`. If you want unlimited, just set it to a high number like `999.000000`.)

4. Save and close the file.
5. **IMPORTANT STEP**: Right-click `GameUserSettings.ini` > Properties > Check `Read-only` > Click Apply then OK.

## Notes
- **Why Read-only?** The game's engine will try to overwrite this file and reset the cap to 60 if it isn't locked.
- It is also worth noting that the game changes language after the fix is applied, or at least it did on my end. If your language changes after the fix, then you can just set it back. It does not seem to change every time you launch the game with the fix applied.
- It is also better if you change your graphics settings before applying the fix, anything you change will not save since this will lock your current settings due to the Read-only attribute.

## How to know if it works
- From my testing, if the fix works then the game will play at a higher framerate than the framerate cap shown in your settings. If the framerate cap in the settings is set to `30` but your game is still playing above that value, then the fix is working. You can also see the attached video for proof. This seems to be normal for other games (e.g., FPS Unlocker for Wuthering Waves and Genshin Impact).
- Video is quite scuffed, threw it together as quickly as I could. The effect is more visible at the end where my FPS reached 140, as opposed to the 120 FPS cap.

[Video](https://youtu.be/fq8tB6uj8wQ)

## Safety
This method of unlocking FPS is just part of how Unreal Engine handles configuration files per user and I was only able to derive it from another project that unlocks the FPS cap in Wuthering Waves. While this method is generally considered safe, modifying internal game files is performed at your own risk. I will not be held liable for anything that happens to your account.
The best I can do is update this repository if something does happen to my account.

<3
