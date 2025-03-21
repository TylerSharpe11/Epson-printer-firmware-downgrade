This repo is for people that want the old version of epson firmware that lets you use 3rd party ink. I got all the info from here: https://www.ifixit.com/Answers/View/741186/Problem+downgrading+the+firmware+of+an+Epson+WF-7840?permalink=answer-841683#answer841683

I just replaced the FWCH67TL.efu file which contains the FWCH67TL.rcx firmware file from FWCH67TL.dmg to final.dmg

So just running final.dmg should run and install the older firmware that works with 3rd party ink. I've only tested this on my Epson WF-7820.



Here's the post with the most recent info by Router Downer:

"Does anyone actually have a copy of the Epson Recovery Mode Firmware tool that isn't the "latest", such as "FWCH67TL_CD08M4.exe"? I'm looking to recover my WF-7820 that was auto-updated today (1/23/2025).

The CD29OB update from 1/3/2023 was applied and of course Epson doesn't seem to archive previous versions (or maybe they do and I couldn't exercise the proper URL path) of the recovery mode firmware at all (not a real shock if their objective is to eliminate prior firmware that is compatible with 3rd party ink).

It seems the Epson Recovery Mode Firmware CD29OB may have been patched to eliminate prior firmware "side loading", so having access to the prior tool versions would be required for self-repair, etc. If you have a different experience, feel free to respond as it's unclear from the current comments if recent recovery comments were from the 1/3/2025 CD29OB update or something just prior.

If you have a proper link, or can provide the tool that'd be great. In theory if they're signed properly for Windows, it shouldn't be an issue versus providing a blind executable without it being signed. Maybe throwing this stuff on a Github repo with up-to-date instructions would be a good solution if iFixit doesn't have something similar.

Thanks!

---

UPDATE 1/26/2025:

Ok,

So if you're dealing with CD29OB drivers and trying to rollback, here's what you do (just follow DaveYVRs instructions, but here are the files you need):

https://ftp.epson.com/drivers/FW_CD08M4.... (this is the old firmware from DaveYVRs instructions, which you get the downgraded driver file from to use in the recovery process - FWCH67TL.rcx).
https://ftp.epson.com/drivers/FWCH67TL_C... (don't use FWCH67TL_CD29OB.exe, which is what the Epson site will default you to by selecting your printer model, your OS and under Firmware -> Recovery Mode Firmware Version CD29OB).
This will allow you to downgrade with the recovery tool, as the CD29OB one patched out the ability to supplant the driver file in some way.

DaveYVRs instructions are good enough to get you through it, just remember to connect the printer via USB, power up the printer, use the "Power, 4, 7, Job Status" and you'll see the recovery mode initiate on the printer screen, copy the FWCH67TL.rcx file into the proper place when the recovery tool is running (but you haven't started the update), start the update (you'll see it copy everything and you can "finish" the process when prompted), set a timer for 15 minutes and eventually your printer will go into Xmas tree mode (flashing lights), just power it off and use as you normally would (for me that would be setup on the Ethernet connection) -- I didn't have to remove any ink cartridges after rebooting it, everything just worked normally.

Epson seems to archive some of the drivers in https://ftp.epson.com/drivers/FILENAME_H... URL path, but some of the older stuff mentioned in this thread are definitely not available in that URL path. I would suggest keeping versions of the drivers and an older version of the recovery firmware tool around in a github repo, or wherever -- really makes this whole thing much easier than relying on Epson to do something consumer-friendly."