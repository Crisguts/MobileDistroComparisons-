Step-by-Step Installation Process for Custom ROM on Galaxy A70
--------------------------------------------------------------

-Overview-
Install any custom ROM (Ubuntu Touch, LineageOS, or similar) on the Galaxy A70.
This solution may or may not work on other devices.
These steps were done using a Windows PC.
All necessary resources can be found in the Resources.txt file of the repositary.
==================================================================================================
Step 1: Gather Required Tools
Downloads:
  Odin (Windows tool for flashing firmware).
  TWRP recovery image for the A70.
  Custom ROM/ZIP file of your choice.
  Patched VBMeta image (optional, for error handling).
  ADB tools (for transferring files).
==================================================================================================
Step 2: Unlock the Bootloader
 1.Enable Developer Options in Settings > About Phone (tap "Build Number" 7 times).
 2.Enable OEM Unlocking in Developer Options.
 3.Reboot to Download Mode (Power + Volume Down + Volume Up).
 4.Unlock the bootloader (this will wipe your data).
==================================================================================================
Step 3: Flash TWRP Recovery
 1.Boot into Download Mode again.
 2.Open Odin on your PC, load the TWRP image into the "AP" section, turn off auto-reboot in options, and start.
 3.Disconnect and immediately boot into TWRP (Power + Volume Up while connecting USB).
==================================================================================================
Step 4: Format and Wipe the Device
 1.In TWRP, go to Wipe > Format Data, type "yes," and confirm.
 2.Perform an Advanced Wipe: Select Cache, Dalvik/ART Cache, and System.
 3.Reboot back into recovery to ensure a clean environment.
==================================================================================================
Step 5: Transfer the ROM/ZIP File
 1.Connect your phone to the PC in TWRP mode.
 2.Use adb push [ROM.zip] /sdcard to copy the ROM/ZIP file to the phone.
 3.Verify the connection with adb devices before transferring.
==================================================================================================
Step 6: Flash the ROM
 1.In TWRP, go to Install, select the ROM/ZIP file from the device's storage.
 2.Swipe to confirm installation.

--------------Optional Step: Fix VBMeta Error------------------
| If the phone fails to boot and shows a VBMeta-related error |
-------Then you must do the following step before Step 6-------

->Flash a patched VBMeta using Odin by loading the TWRP image into the "USERDATA" section and 
-> turning off auto-reboot in options, and clicking start.  
->This disables Verified Boot, allowing the custom ROM to function.                                  
==================================================================================================
Step 7: Reboot and Test
 1.Reboot into the system.
 2.Verify the ROM’s functionality by checking settings, connectivity, and basic features.
==================================================================================================

---------------------Hooray !! You successfully changed your A70's OS-----------------------------

