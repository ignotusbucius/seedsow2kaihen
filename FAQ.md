# FAQ

**Can I just put something on the SD card and jailbreak?**
No. The exploit lives in Seedsow's save data; the SD card only holds the kaiHEN files it loads at the
end. Getting the save on needs a hacked Switch 1 and Nintendo's save transfer, or another exploit game
on the Switch 2 (README step 1). After that one-time setup and one PC session, no PC or Switch 1 is
needed.

**Can I still transfer the save from a Switch 1?**
Unclear. Success reports stop before firmware 23.5.0 came out, and Nintendo asks for the latest system
update on both consoles. README step 1 has the details, plus routes with no Switch 1 at all
(SmileBASIC 4, Civilization VII).

**Does it survive a reboot?**
No, kaiHEN runs in RAM. After every reboot, open Seedsow, press A and wait for READY (step 5). The save,
the SD files and the Switch 1 game package from step 6 all stay.

**Do I need a Switch 2 game?**
No. Stock kaiHEN only opens hbmenu from Switch 2 games; with step 6, Switch 1 games work too, and
Switch 2 games keep working.

**Which firmware?**
Everything was tested on 23.0.1. Firmware 23.5.0 (2026-11-10) is reported to patch part of the chain,
so don't update the Switch 2. alula's README notes that once the 23.0.1 window closes, getting a
launcher save on needs another entry point such as SmileBASIC 4 or Civilization VII 1.0.0
([CivSwitch](https://github.com/Gezine/CivSwitch)).

**Which SD card?**
Any microSD, Express not needed. FAT32, or exFAT if the console has the exFAT update.

**Every attempt ends with "0 pointer candidates".**
Seen on one console as a clean stop with no damage. A hard reboot and a fresh try worked every time.

**The chain says "required SD files missing".**
Do README step 4. The chain needs `bootstrap.bin`, `ro/main`, `hen/main` and `game/main` under
`/kaihen/bin/`. The kit's PC mode doesn't add the first two.

**I held a button while starting Seedsow and nothing happened.**
On the console we tested, a button already held when the game starts isn't seen until you let go and
press it again. If a menu asks for a button at startup, start the game first, then press it.

**Loading a save slot loaded the wrong one.**
In Seedsow's LOAD grid, the first d-pad press only moves the cursor onto slot 1, so slot N needs one
more press than you'd expect. Check the highlighted slot before confirming.

**Can I use my own kaiHEN build?**
Yes. The chain only checks that `/kaihen/bin/hen/main` exists and starts whatever is there, so a custom
HEN like the Switch 1 titles one drops right in. Keep a copy: the kit's Update kaiHEN and Prepare SD
overwrite it.

**Will emulators run well from a Switch 1 game?**
Not measured. Homebrew started from a Switch 1 game most likely gets Switch 1 memory and speed limits.
Use a Switch 2 game for heavy homebrew if you have one.
