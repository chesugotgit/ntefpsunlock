# Neverness to Everness (NTE) - Override the framerate cap by modifying GameUserSettings.

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
- **Why Read-only?** The game's engine will try to overwrite this file and reset the cap to 60 if it isn't set to Read-only.
- It is also worth noting that the game might change languages after the override is applied, or at least it did on my end. If your language changes after the change, then you can just set it back. It does not seem to change every time you launch the game with it applied (check below if it does).
- **It is also better if you change your graphics settings before applying the change, anything you change after applying the override will not save since this will lock your current settings due to the Read-only attribute.**

## Validation / Checking if it works
- The override is applied correctly if your game is running at a higher framerate than the one that is shown in your settings. This value resets back to `30` after the override.
- Video is quite scuffed, threw it together as quickly as I could. The effect is more visible at the end where my FPS reached 140, as opposed to the 30 FPS cap shown in my settings menu.

[Video](https://youtu.be/fq8tB6uj8wQ)

## Graphics Settings Reset
- For situations where the game might reset your graphics after you applying the override, you'll need to do the following (Assuming you've already applied the override):
1. While the game is open, go back to the folder where `GameUserSettings.ini` is located (Press `Win + R`, paste the following, and hit Enter: `%LocalAppData%\HT\Saved_Global\Config\Windows`).
2. Right-click `GameUserSettings.ini` > Properties > Check `Read-only` > Click Apply then OK. (**Disable** it if it was enabled to apply the change, if it is disabled, then leave it be).
3. Go back to the game and change your graphics settings (to make sure it saves, exit out of out the graphics settings and go back into the overworld).
4. Go back to the folder where `GameUserSettings.ini` is located then right-click `GameUserSettings.ini` > Properties > Check `Read-only` > Click Apply then OK (`Read-only` should now be **on**).
5. Restart your game and double-check if the unlocker and your graphics options have applied correctly.
- **NOTE: You do not need to remove the lines you added at the bottom to do this. Leave it be and change your settings. If you did, go back to step 1 in applying the override.**


## Safety
This method of unlocking FPS is just part of how Unreal Engine handles configuration files per user and I was only able to derive it from another project that unlocks the FPS cap in Wuthering Waves.

While this method is generally considered safe, modifying internal game files is performed at your own risk. I will not be held liable for anything that happens to your account.
The best I can do is update this repository if something does happen to my account.

<3
