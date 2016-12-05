Install documentation & automation
----------------------------------
- [ ] Allow custom install path vs. forcing C:\Workspace - see [deepdrive](https://github.com/crizCraig/deepdrive/blob/master/README.md) install
- [ ] Automate xbox 360 config
- [x] Copy ScriptHookProxy.asi into GTAV folder in install.py
- [x] Copy relevant deepdrive sections
- [x] Add install.py to README.md
- [x] Add "Grand Theft Auto V" and "grcWindow" to TightVNC server configuration
- [x] Install vjoy - default config should work
- [x] Install xbox360ce with [this ini](https://gist.github.com/crizCraig/f680f65653641412eba28c3c47421bcf)
- [x] Install game binaries from known location
- [x] Use static saved game files from [here](https://www.dropbox.com/sh/k1osqcufsubo754/AADCeXM4I1iYRz19bdO12pOba?dl=0)
- [x] Copy ScriptHookProxy.asi into GTAV folder
- [x] Separate common windows steps from StarCraft into vnc-windows/INSTALL.md
- [x] Make sure game runs in borderless mode.\
- [x] TODONT (doesn't work on windows server 2012) Buy GTAV Rockstar warehouse or look for discounts at places like http://www.cdkeys.com/pc/games/grand-theft-auto-v-5-pc-cd-key and https://www.g2a.com/grand-theft-auto-v-cd-key-global.html?___store=englishus

Runtime
-------
- [ ] Return forward-vector for deriving comfort metric
- [ ] Pull steering and throttle from memory for artificial demonstrations (Aitor's DeepGTAV has this worked out, should update scripthook to get memory offset named functions)
- [ ] Lazy load center-of-lane init via remote settings as it delays loading and may have stability issues
- [ ] Allow booting straight into game on EC2 without an initial RDP (may just require tscon connect on startup)
- [ ] Support hard reset (restart GTAV process)
- [ ] Investigate the location of line points on some "strange" urban roads (for center of lane reward)
- [ ] Derive reward from distance to some goal
- [ ] Use standalone version with offline flag
- [ ] Get distance to traffic objects with [this](https://docs.google.com/document/d/1RftRxeoOdGSleWK0wgewHAoMHBqpXGXXwi8UlH92_KE/edit?usp=sharing)
- [ ] Get distance to nearby cars
- [ ] Get distance to nearby pedestrians
- [ ] Add child pedestrians
- [ ] Get distance to nearby animals
- [ ] Get distance to all nearby collidables
- [ ] If auto-update happens, auto-rollback.
- [ ] Refocus window every once in a while (SC does this)
- [ ] Support center of single lane dirt roads like the one [here](https://www.dropbox.com/s/gb5mj5qdymqem67/Screenshot%202016-10-28%2011.48.35.png?dl=0)
- [ ] Allow driving reward-mode from agent (currently agent setting is ignored and reward-mode is set in GTAVController.exe parameters)
- [x] Get distance to center of lane
- [x] Fix ASI startup issue (currently need to reload mods with Ctrl+R after game has started)
- [x] Handle Social Club login blocking game load -- Launching through steam fixes this
- [x] Change to hood camera programmatically (saved game does not reliably set this)
- [x] Derive reward on-road, and whether or not we hit something
- [x] Get video streaming to universe (1FPS though)
- [x] Reset mod options like Cops / peds not shooting player, car indestructible, every 10 seconds
- [x] Send steering and throttle via websockets from universe
- [x] Start game with run_vnc_env.py
- [x] Cleanup game executables in run_vnc.py 
- [x] Create ScriptHookProxy.asi to call scripthook stuff and share memory with GTAVController.exe with you'll now be able to debug and you won't have to reload / copy constantly every change.
- [x] Start GTAV controller in run_vnc_env.py
- [x] Load story mode
- [x] Load saved game
- [x] Check that we're in game before every keystroke (okay since car controls are done via joystick)
- [x] Do quicker checks for saved memory
- [x] See if switching to standalone version in offline mode needs online DRM check [yes it does](https://www.amazon.com/Grand-Theft-Auto-V-PC/product-reviews/B00KVXB5YQ/ref=cm_cr_arp_d_viewopt_kywd?ie=UTF8&showViewpoints=1&sortBy=recent&pageNumber=1&filterByKeyword=social+club)
- [x] Send controls for steering and throttle through vjoy
- [x] Use the connection_set in the broadcast example
- [x] Test the connections out int GTAV controller
- [x] Vendor vjoy
- [x] See if we need to set all vjoy axes to zero