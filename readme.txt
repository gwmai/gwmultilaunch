=Guild Wars Multi-Launch=

Open Source License: GPLv3

==Summary==

Launching multiple copies of Guild Wars.
(no modifications to Guild Wars files!)

==Requirements==

  # Guild Wars
  # .NET Framework 2.0 or equivalent
  # Windows XP, Vista, or 7

==Usage==

Copies of the Guild Wars folder need to be made. The number of copies depends on how many copies you would like to have open at once. You will only need to make 1 extra copy to be able to run two copies side by side.

After these copies are made, add them to the list. Then, make the multi-launch enabled shortcuts which are good for launching multiple copies of Guild Wars. Or just select the game and launch it from the gui.

(if you are using Vista/7 and having trouble running multiple copies see notes)

Concisely:

  # Make copies of Guild Wars folder (just need gw.exe and gw.dat)
  # Add the gw.exe(s) to the list
  # Double click item to launch
    * or click "Launch" button
    * or make a shortcut for external launching

Guild Wars Updates: When there is an update, you will need to launch a second time if you have multiple Guild Wars updating at the same time. See gw.dat question in the FAQ for details.

Texmod Usage: Check the FAQ section.

==Basic Controls==

  * Add - add the location of an existing copy
  * Remove - remove selected copy from list
  * Make Copy - make a copy (make sure to create new folder in dialog)
  * Launch - start the selected copies
  * Make Desktop Shortcut - add a desktop shortcut to launch selected copy

==Expert Controls==

  * Set Registry Path - path should be set before manually starting a specific install
  * Clear Mutex - closes the mutex handle under all live gw.exe processes
  * Open Texmod - attempts to locate Texmod and open
  * Force gw.dat unlock - read warning message... useful if you are out of diskspace and need to desperately mule without extra copies

===Launch Sequence===

  # Set new gw path in registry
  # Mutex cleared from all gw.exe processes
  # Launch gw copy

==Vista/Win7 Quirk==

Any guild wars copies installed to:
C:\Program Files or C:\Program Files (x86) <--folder only exists in 64-bit window installs

seem to require special permissions when started. (at least on Vista-64, may be true for Vista and Win7 32bit as well)

Specifically gw.exe needs to be ran as administrator to access gw.dat. When gw.exe is ran as administrator, in Vista and Win7, Guild Wars Multi-launcher ALSO needs to be ran as administrator for it to be able to close handles in the gw copy that ran as admin.

Vista and Win7 are tricky in that, once you approve a program to run as admin, it doesn't really ask you again for a while. Even if you move it, it still seems to remember to run as admin. Don't know if this lasts the session or not.

Solutions:
1) Run Guild Wars Multi-Launcher in admin mode (right click gwmultilaunch.exe-> run as admin)

Running gwml in admin mode as well puts it on equal footing with gw.exe that was run as admin. This allows it to close the mutex which prevents more gw.exes from launching.

==FAQ==

Q: Do I have to always use the launcher or the special shortcuts?

A: No, you only need to use the launcher or shortcuts when you wish to launch multiple copies of Guild Wars.

Q: Why do I get a "gw.dat is locked" message?

A: This is often the case if you launch the copy without setting the registry path properly. If you are planning to launch multiplecopies, the registry path must be set properly to avoid conflicts. Gw.exe will always use the path found in the registry to locate gw.dat.

Q: When I try to launch muliple copies at once through the launcher, not all of them launch. Why?

A: The default delay between copies is current set to 3000 milliseconds in the "regdelay" setting in your ini file. Increase this value for slower computers since Guild Wars may need more time to read the value off the registry before it is set to something else for the next copy.

Q: What is a Mutex?

A: Simple answer, a flag that gw.exe puts up so new gw.exe processes know to not launch. Long answer, check wikipedia.

Q: How do I use Texmod with this?

A: To launch a Texmoded copy:
   # Select the copy you will be launching and click "Set Registry Path"
   # Click "Clear Mutex"
   # Open Texmod and launch the copy

Q: How do I report a bug?

A: Please report all bugs at http://code.google.com/p/gwmultilaunch/issues/list.

==URL==

http://code.google.com/p/gwmultilaunch/

==Contributors==

  * IMKey
  * satomz - icon art!

==Special Thanks==

  * moriz - thank you for being the brave soul to test this in windows 7
  * Alexander Burn Victim - thank you for testing in vista 64-bit
  * Aciid Bu5t0r - thank you for bringing up the idea of forcefully unlocking gw.dat

==History==
v0.5RC (2009/05/22)
  * Dual releases now, one for 32-bit windows, one for 64-bit windows
  * Rewrote large portion of handle managing code to be 64-bit compatible
  * Misc speedups in HandleManager
  
v0.45b (2009/05/17)
  * Fixed bug introduced with implementing gw.dat unlocking affecting normal operations in Vista 64-bit
  
v0.42b (2009/05/16)
  * Fixed "Make Copy" issue with Template folders not being found under Guild Wars folder
  
v0.4b (2009/05/16)	
  * First beta. Feature lock for now. Only bugs fixes until first stable release.
  * Added ability to drag and drop into list of copies
  * Added ability to make copies of Guild Wars from the gui.
  * Added super experimental "Force gw.dat unlock" for launching the same copy multiple times (gw.dat corruption possible)
  
v0.35a (2009/05/14)	
  * Added delay back in when launching multiple copies

v0.3a (2009/05/14)		
  * Detect initial copy of Guild Wars automatically
  * Error dialog on launching same copy of Guild Wars
  * Added icons
  * Took out registry path change back to be more compatible with updates.

v0.2a (2009/05/12)
  * Fixed registry key location issue for Win Vista/7
  * Fixed unicode conversion for Win7

v0.1a (2009/05/09)
  * Initial Release

==License==

This software is open source licensed under GPL v3. Anyone is free to view the source. The source is available at the project url. It is a C# solution for Visual Studio 2005.