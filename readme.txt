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

Copies of the Guild Wars folder need to be made beforehand. The number of copies depends on how many copies you would like to have open at once. Most likely, you will only need to make 1 extra copy to be able to run two copies side by side.

After these copies are made, add them to the list. Then, make the multi-launch enabled shortcuts which are good for launching multiple copies of Guild Wars. Or just select the game and launch it from the gui.

Concisely:

  # Make copies of Guild Wars folder (just need gw.exe and gw.dat)
  # Add the gw.exe(s) to the list
  # Click "Make Shortcut" and open the shortcut
    * or Hit Launch button to start Guild Wars

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

===Launch Sequence===

  # Set new gw path in registry
  # Mutex cleared from all gw.exe processes
  # Launch gw copy

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


==History==
v0.4b (2009/05/16)	
  * First beta. Feature lock for now. Only bugs fixes until first stable release.
  * Added ability to make copies of Guild Wars from the gui.
  * Added super experimental "Force gw.dat unlock" for launching the same copy multiple times (warning, this may corrupt your gw.dat file)  
  
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