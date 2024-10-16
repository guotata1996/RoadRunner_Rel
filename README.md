# RoadRunner Release Repository
[Download RoadRunner v0.8](https://github.com/guotata1996/RoadRunner_Rel/releases/tag/v0.8)

## About
A desktop road network editor that makes [ASAM OpenDRIVE](https://www.asam.net/standards/detail/opendrive/)-format maps. Compared to commercial mapping software, RoadRunner is intended for casual users and hobbiests, providing free and easy experience without learning curve or $$ investment.

This repository hosts RoadRunner's public releases. The source code remains private while more features are still being brought in.

![RoadRunner](roadrunner.png "RoadRunner")

## Quick Manual
### Menu
- File
  - New: Reset the application to blank state. All unsaved changes will be lost.
  - Open: Load an .xodr map. Only those exported from RoadRunner are supported.
  - Save: Save current map in .xodr format.
  - Background: Choose an image as background. Recommand at least 1000x1000 pixels.
  - Preference: Application-wide options and About.
- Edit
  - Undo
  - Redo
  - Verify Now: Checks app state and reports any inconsistency, i.e. bug. If "Always Verify" is set to ON inside Preference, this check will run upon each edit. 
  - Toggle Simulation: Randomly spawns running cars. Used for routing graph verification only; not a traffic simulation. 
- Replay
  - Save: Save actions since startup or last New map to a .dat file. Won't work if actions contain opening an .xodr map (this is a planned feature).
  - Debug: Load saved actions (.dat) and start playing at highest rate.
  - Watch: Load saved actions (.dat). In the new dialog, hit play `>` button to play/pause, `1` to step, and `|<` to start over. Double click on a list entry to toggle break point. Playback will be in real-time, i.e. will last (roughly) how long it took to record.

### Modes
Modes are best demonstrated in [demo videos](#demo) below.
- ![Road mode](resources/icons/road_mode.png "Road mode") Create roads with auto-generated transitions and junctions.
- ![Ramp mode](resources/icons/lane_mode.png "Ramp mode") Manually make junctions and highway ramps.
- ![Modify mode](resources/icons/modify_mode.PNG "Modify mode") Two clicks on the same road, then apply a new profile to the selected segment. Double-click to select entire length.
- ![Destroy mode](resources/icons/destroy_mode.png "Destroy mode") Two clicks on the same road, then destroy this segment. Double-click to destroy entire length.
- ![View mode](resources/icons/view_mode.png "View mode") Drag to pan. Allows traffic simulation.

### Elevation options
- ![Create above](resources/icons/bridge.png "Create above") Create roads above existing.
- ![Create flat](resources/icons/flat.png "Create flat") Create roads to forms junctions with existing.
- ![Create below](resources/icons/tunnel.png "Create below") Create roads below existing.

### Mouse
- Left button: Select
- Middle button: 
  - Drag: Pan
  - Scroll: Zoom
- Right button:
  - Click: Cancel
  - Drag: Pick
### Keys
- Ctrl: hold + mouse scroll to switch elevation modes.
- Enter: Confirm road edits.
- Escape: Cancel road edits.
- Key_A: Cycle to the next overlapping road, where multiple roads overlap.
- Key_I: Print (to the console) more details of the hovering road.


## Demo
### v0.8 - Bridges and road markings
![Bedford](resources/bedford_left.png "smooth")
- [OpenDRIVE map](resources/bedford_0_8.xodr)
- [Background image](resources/bedford_background.PNG)

## History
### v0.6 - smooth curves
![Bedford](resources/smooth_ramps.JPG "smooth")
- [OpenDRIVE map](resources/interchange_smooth.xodr)
- [Action Replay](resources/interchange_smooth.dat)

### v0.5
Click on images to check out the **video**.

[![Basics](https://img.youtube.com/vi/V2m4WTE1YkU/0.jpg)](https://www.youtube.com/watch?v=V2m4WTE1YkU)

Please check out [Quick manual](#menu) for how to use the attachment below. 

- [OpenDRIVE map](resources/basics.xodr)
- [Action Replay](resources/basics.dat)

[![Hwy exit](https://img.youtube.com/vi/Bl3_kxfEm74/0.jpg)](https://www.youtube.com/watch?v=Bl3_kxfEm74)
- [OpenDRIVE map](resources/hwy_exit.xodr)
- [Action Replay](resources/hwy_exit.dat)

### Bedford interchange
![Bedford](resources/bedford.JPG "Bedford")
[OpenDRIVE map](resources/bedford.xodr)

## Known issues
- Vehicle & slope road surface may display in wrong order.
- Creating multi-layer bridges will be difficult.

If you find anything bothering or can't get around with, reporting is welcome through Github issues. Please attach the .xodr map and .dat action record if possible.

## Disclaimer
This software is provided as-is, free to use. The author assumes no responsibility in any issue that results in any kind of loss.

## Credits
[OpenDRIVE online viewer](https://odrviewer.io/) 

[libOpenDRIVE](https://github.com/pageldev/libOpenDRIVE)