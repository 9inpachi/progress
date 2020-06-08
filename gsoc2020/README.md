# Progress of Phoenix for GSoC 2020

For the moment, the work is being done on different branches at [https://github.com/9inpachi/phoenix](https://github.com/9inpachi/phoenix).
The work in progress or the new features should be scattered in branches with the "wip-" prefix.

## Day 01 - 30 May 2020 - Sat
- [x] Added toggle for wireframing detector geometries
- [x] Try out different ways for improving wireframing representation and settle with reducing the opacity

## Day 02 - 31 May 2020 - Sun
- [x] Set up to get metadata of experiments
- [x] Get loader specific metadata (LHCb loader for now)

## Day 03 - 01 Jun 2020 - Mon
- [x] Start improvement of overall GUI
- [x] Revamp UI menu icons
- [x] Improve the look of UI menu
- [x] Add toggle for switching main view from the UI menu

## Day 04 - 02 Jun 2020 - Tue
- [x] Add toggle to UI menu for switching between orthographic and perspective views
- [x] Add icons to preset views in UI menu and remove orthographic checkbox
- [x] Add control to UI menu for zooming in and out with a smooth effect (using TWEEN)
- [x] Make zoom controls zoom both overlay and main view in and out with left mouse button hold

## Day 05 - 03 Jun 2020 - Wed
- [x] Button for hiding and showing the UI menu (toolbar)
- [x] Fix the expand icon and make it consistent with the other icons
- [x] Replace the navigation bar with a single phoenix icon
- [x] Handle inconsistencies in metadata that can appear in event data

## Day 06 - 04 Jun 2020 - Thu
- [x] Set up the info panel for merge
- [x] Retain event display aspect ratio
- [x] Add toggle to overlay view for a fixed overlay
- [x] Collaborate on issues and ideas
- [x] Look into GitHub actions for automated release

## Day 07 - 05 Jun 2020 - Fri
- [x] Have a video meeting with Ed
- [x] Look for ways to get JSON geometry
- [x] Convert a group of deprecated JSON geometries to GLTF
- [x] Debug why geometries have bugs in Phoenix (because of scaling)

## Day 08 - 06 Jun 2020 - Sat
- [x] Try out (a lot) of ways to improve geometry
- [x] Use four updated directional lights to improve lighting (can also use camera light - TBD)
- [x] Find out how geometries can be smoothen
- [x] Use MeshPhongMaterial with 0 shininess for geometries (huge improvement)
- [x] Add toggle for closing clipped geometries and a slider for scaling all detector geometry (for debugging)

## Day 09 - 07 Jun 2020 - Sun
- [x] Shift close clipped geometries option to UI menu
- [x] Try fixing closing of clipped geometries by toggling the clipping option (does not work - works manually)
- [x] Scale ATLAS geometries to normal size (not implemented in Phoenix)
- [x] Further debugged renderer and cameras for geometry and found that the camera's frustum near plane needs to be larger (fixes geometry bugs)