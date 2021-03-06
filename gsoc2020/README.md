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
- [ ] Try fixing closing of clipped geometries by toggling the clipping option (does not work - works manually)
- [x] Scale ATLAS geometries to normal size (not implemented in Phoenix)
- [x] Further debugged renderer and cameras for geometry and found that the camera's frustum near plane needs to be larger (fixes geometry bugs)

## Day 10 - 08 Jun 2020 - Mon

- [x] Separate ATLAS geometry parts in glTF format
- [x] Update glTF loading to support scaling of geometries and specification of side
- [x] Option in UI menu for closing clipped geometries
- [x] Option for scaling the complete detector (for debugging?)

## Day 11 - 09 Jun 2020 - Tue

- [x] Update to use a single directional light that follows the camera (better performance)
- [x] Update glTF loading to use the already existing geometry side specified in the glTF file
- [x] Move the zoom controls to controls manager
- [x] Highlight collection info on event object select

## Day 12 - 10 Jun 2020 - Wed

- [x] Link collection info panel with the scene
- [x] Move camera to object from collection info
- [x] Debug why the quality of Phoenix scene is low
- [x] Try setting antialiasing and pixel ratio for improving resolution (does not work)
- [x] Add FXAAShader to improve rendering of objects (works but quality not good)

## Day 13 - 11 Jun 2020 - Thu

- [x] Add option for highlighting objects from the collections info panel
- [x] Make collections info panel height dynamic so resizing the overlay panel resizes the collections info table
- [x] Add icons to collection info table for "look at object" and "highlight" object functions
- [x] Fix LHCb loader bug by handling undefined event data elements

## Day 14 - 12 Jun 2020 - Fri

- [x] Make collections info selection work for muons and some misc improvements
- [x] Learn and work on GitHub actions for Phoenix deployment
- [x] Write an action for deploying Phoenix for every push to master branch
- [x] Write an action for releasing Phoenix for pushing to a tag

## Day 15 - 13 Jun 2020 - Sat

- [ ] Weekend

## Day 16 - 14 Jun 2020 - Sun

- [ ] Weekend

## Day 17 - 15 Jun 2020 - Mon

- [x] Remove options for closing clipped geometries and scaling detector from branch `wip-atlas-geom`
- [x] Fix "look at object" for Tracks, Hits and Muons (using bounding sphere for Tracks and Hits)
- [x] Add loader for loading geometries from JSON
- [x] Fix HSF/phoenix#73 by using a combination of Tube and Line for tracks

## Day 18 - 16 Jun 2020 - Tue

- [x] Improve lights and add parameter for using camera lights in SceneManager
- [x] Study Runge-Kutta methods for implementation
- [x] Update metadata to optionally use label and value
- [x] Fix some minor typos and rectify PRs from `wip-collections` (selection from collections info) and `wip-atlas-geom` (improvement of geometries) branches

## Day 19 - 17 Jun 2020 - Wed

- [x] Remove glTF ATLAS geometries (keep a backup)
- [x] Minor code improvements
- [x] Simplify experiment info template code
- [x] Port Runge-Kutta to typescript

## Day 20 - 18 Jun 2020 - Thu

- [x] Document and improve Runge-Kutta port
- [x] Fix overlay `title` property by changing it to `overlayTitle` to avoid overlap with HTML `title` attribute
- [x] Fix info logger glitches because of reversing array for each render
- [x] Fix depthTest not working for event data after updating Tracks to use a combination of `Tube` and `Line`

## Day 21 - 19 Jun 2020 - Fri

- [x] Minor fixes to the Runge-Kutta port
- [x] Try making Runge-Kutta work for ATLAS/Phoenix loader (the current JSON format for ATLAS does not have the required track properties)
- [x] Try making Runge-Kutta work for LHCb loader (three dimensional momentum causing problems but we do get some incorrect lines)
- [x] Try making Runge-Kutta work for CMS loader (could not find data for tracks momentum)

## Day 22 - 20 Jun 2020 - Sat

- [x] Email Andreas to ask some questions regarding the Runge-Kutta implementation
- [ ] Weekend

## Day 23 - 21 Jun 2020 - Sun

- [ ] Weekend

## Day 24 - 22 Jun 2020 - Mon

- [x] Fix cuts not working for Tracks and assign uuid to object params (was using reference before)
- [x] Look up formulas for using transverse momentum (could not find anything useful)
- [x] Again give a try to making Runge-Kutta work for LHCb loader (no success)
- [x] Again give a try to making Runge-Kutta work for CMS loader (no success)

## Day 25 - 23 Jun 2020 - Tue

- [x] Set up CMS loader
- [x] Improve event metadata collection in PhoenixLoader
- [x] Set up CMS experiment section with test event data
- [x] Support for objects as hits parameters in `PhoenixObjects.getHits(hitsParams)`
- [x] Update CMS loader to get and process all collections of clusters from the event data
- [x] Get CMS specific event metadata

## Day 26 - 24 Jun 2020 - Wed

- [x] Update CMS loader to get and process any collection of tracks from the event data (there is either `Tracks_V1`, `Tracks_V2` or `Tracks_V3`)
- [x] Study tracking in ATLAS
- [x] Convert local perigee params of tracks to global params
- [x] Try making Runge-Kutta work for ATLAS (we do extrapolate event-like tracks)

## Day 27 - 25 Jun 2020 - Thu

- [x] Support for Jets collections in CMS loader
- [x] Support for CaloClusters in CMS loader and other improvements
- [x] Find out that antialiasing works on previous Phoenix version (three.js r104)
- [x] Debug antialiasing in the current version and find fix (because of `EffectComposer` being rendered after the main renderers)

## Day 28 - 26 Jun 2020 - Fri

- [x] Update CMS loader to use a common function and improve `PhoenixObjects`
- [x] Add support for all possible collections of tracks in CMS
- [x] Support for custom CMS objects (MuonChambers)
- [x] An example of using a custom object type with Phoenix

## Day 29 - 27 Jun 2020 - Sat

- [ ] Weekend

## Day 30 - 28 Jun 2020 - Sun

- [ ] Weekend

## Day 31 - 29 Jun 2020 - Mon

- [x] Analyze the current Phoenix JSON format
- [x] Add RungeKutta tracks as duplicate collections for debugging
- [x] Optimize loading ".ig" files and move the functions to CMS loader
- [x] Ability to read and get all events from an ".ig" file

## Day 32 - 30 Jun 2020 - Tue

- [x] Detailed video call with Edward
- [x] Debug RungeKutta tracks
- [x] Start making a script for loading and converting encoded JSON geometries to glTF
- [x] Add geometry to CMS, add CMS experiment card and make the pull request for CMS integration

## Day 33 - 01 Jul 2020 - Wed

- [x] Convert tracer geometries to glTF
- [x] Automated export for encoded JSON geometries
- [x] Try making Jets scalable and increase maximum Jet length to 3000 (2000 previously)
- [x] Scale Jets by removing current Jets and generating new ones with higher energy (has bugs)

## Day 34 - 02 Jul 2020 - Thu

- [ ] Try fixing bugs for making Jets scalable with the remove/add approach
- [x] Explore and implement more options for scaling Jets - tried a lot but most do not work
- [x] Write simplistic logic for scaling Jets by scaling `Mesh`, resetting position using scale and then changing the position again
- [x] Fix and improve event data depthTest

## Day 35 - 03 Jul 2020 - Fri

- [x] Analyze event data JSON to check the structure
- [x] Propose a new event data JSON format for reducing event data size
- [x] Implement conversion of current event data JSON to new event data JSON
- [x] Implement conversion of new event data JSON to event data JSON used by Phoenix framework

## Day 36 - 04 Jul 2020 - Sat

- [ ] Weekend

## Day 37 - 05 Jul 2020 - Sun

- [x] Generalize `ControlsManager.lookAtObject` to make it work with any kind of object

## Day 38 - 06 Jul 2020 - Mon

- [x] Add support in CMS for loading all events from ".ig" file in Phoenix
- [x] Support for multiple events in new event data format
- [x] Start working on experiment controls
- [x] Think of a proper architecture for experiment control item

## Day 39 - 07 Jul 2020 - Tue

- [x] Completely style experiment control item
- [x] Work towards architecture for dynamically adding children and config
- [x] Create `ConfigCheckbox` for experiment control item config
- [x] Support for toggle, children and config in experiment control item (not working yet)

## Day 40 - 08 Jul 2020 - Wed

- [x] Debug issues with experiment controls
- [x] Use `ChangeDetectorRef` for detecting changes to experiment controls after adding children and configuration
- [x] Make toggle functions work for experiment controls
- [x] Make adding configuration to experiment controls simple

## Day 41 - 09 Jul 2020 - Thu

- [x] Make custom config slider and config checkbox for experiment controls
- [x] Implement working experiment controls in the playground
- [x] Implement experiment controls in the UI service
- [x] Improve custom config slider's code and style
- [x] Make it easier to incrementally add configuration and children by returning valid objects through `addChild` and `addConfig`
- [x] Add options for removing experiment control items and their children

## Day 42 - 10 Jul 2020 - Fri

- [x] Make experiment controls optional in UI service
- [x] REARCHITECT THE EXPERIMENT CONTROLS
- [x] Use a node based structure for experiment controls which is simpler and easily extendable
- [x] Add tree level identification to experiment controls and make other major changes to experiment controls

## Day 43 - 11 Jul 2020 - Sat

- [ ] Weekend

## Day 44 - 12 Jul 2020 - Sun

- [ ] Weekend

## Day 45 - 13 Jul 2020 - Mon

- [x] Add option to change the visibility of detector children so that children can be made visible even if parent is invisible
- [x] Try out different experiment controls depth identification styles and settle with left border with margin on children
- [x] Use a common label for all config types
- [x] Add configuration option for color

## Day 46 - 14 Jul 2020 - Tue

- [x] Cannot keep state of configuration components because using ngIf and if we don't use ngIf then lots of computing required.
- [x] Rename `experiment-controls` to `phoenix-menu`
- [x] Include configuration for changing color of event data
- [x] Finalize styling of phoenix menu

## Day 47 - 15 Jul 2020 - Wed

- [ ] Moved to weekend because had an interview

## Day 48 - 16 Jul 2020 - Thu

- [x] Change new event data format (the one that uses types) to declare parameters/types for each object type collection separately
- [x] Find that the new event data format is not actually any good (was comparing the minified version)
- [x] Move pheonix menu to the right
- [x] Make dat.GUI menu optional and disabled by default
- [x] Support for icons in phoenix menu

## Day 49 - 17 Jul 2020 - Fri

- [x] Add phoenix menu to ATLAS and all other experiments
- [x] Remove custom checkbox configuration for phoenix menu since its redundant for the latest iteration
- [x] Final improvements to phoenix menu
- [x] Open pull request for phoenix menu and write all details including usage

## Day 50 - 18 Jul 2020 - Sat

- [x] Start integration of JSRoot (tried a lot of ways)
- [x] Try integrating JSRoot by globally adding scripts to `index.html` (doesn't load extra required scripts like `?geom`)
- [x] Try integrating JSRoot by adding scripts to `angular.json` (not ideal because we don't have to have the scripts available throughout the application)
- [x] Try integrating JSRoot with requirejs (not ideal either because we have to include requirejs first for JSRoot to define modules)
- [x] Try different ways of using `ngx-script-loader` for dynamically loading the required scripts at run time (only loaded when required)

## Day 51 - 19 Jul 2020 - Sun

- [x] Synchronize JSRoot load with async await
- [x] Make a function for loading JSRoot once and use that (JSROOT becomes available in a callback function)
- [x] Make a custom function for loading JSRoot scripts (and not use `ngx-script-loader`)
- [x] Transform JSRoot script loader to a generalized script loader

## Day 52 - 20 Jul 2020 - Mon

- [x] Add functions for loading JSRoot geometry from `.json.gz` and `.root` and use `.json.gz` geometry for CMS
- [x] Preserve state of different phoenix menu elements
- [x] Try getting event data from `.root` file
- [x] Analyze JSRoot objects for relevant data

## Day 53 - 21 Jul 2020 - Tue

- [x] Analyze JSRoot objects for specific geometry
- [x] Analyze JSRoot objects for running C scripts (can only be done through painter)
- [x] Analyze JSRoot objects TTree and TList for extracting event data (again only processed by the painter)
- [x] Deflate JSRoot geometry colors
- [x] Add parameter to load double sided JSON geometry

## Day 54 - 22 Jul 2020 - Wed

- [x] Go through JSRoot source code and check how event data is drawn
- [x] Go through the JSRootPainter for possible event data leads
- [x] Create `JSRootEventLoader` for loading event data from ".root" files
- [x] Set up to get tracks and hits from event data the ".root" file
- [x] Deeply analyze JSRoot code and port a different solution for extracing and using positions of `TEveTrack`s in phoenix format

## Day 55 - 23 Jul 2020 - Thu

- [x] Improve code and directly use `tracks.fP` to get track positions instead of using `BufferAttribute`
- [x] Don't sort track positions because they cause problems for tracks with returning curves
- [x] Process ".root" file and get hits data from the file and convert it to phoenix format
- [x] Add support for `TGeoTrack`s to `JSRootEventLoader`

## Day 56 - 24 Jul 2020 - Fri

- [x] Optionally make geometry initially invisible and visible on demand from the phoenix menu (`fix-geometry-on-demand`)
- [x] Make ATLAS geometry calorimeters invisible by default
- [x] Finalize JSROOT implementation for loading geometry from ".root" and ".json.gz"
- [x] Finalize JSROOT event loader for loading different tracks and hits

## Day 57 - 25 Jul 2020 - Sat

- [x] Final exam

## Day 58 - 26 Jul 2020 - Sun

- [x] Final exam

## Day 59 - 27 Jul 2020 - Mon

- [x] Add options for making geometry initially invisible for geometry loaded from JSROOT
- [x] Fix failing tests

## Day 60 - 28 Jul 2020 - Tue

- [x] Identify phoenix menu's geometries loading bugs and debug them
- [x] Fix phoenix menu's bug by properly clearing and redefining phoenix menu in UI service
- [x] Final exam

## Day 61 - 29 Jul 2020 - Wed

- [x] Final exam and family trip

## Day 62 - 30 Jul 2020 - Thu

- [x] Family trip

## Day 63 - 31 Jul 2020 - Fri

- [x] Family Trip

## Day 64 - 01 Aug 2020 - Sat

- [x] Eid
- [x] Start learning and working on angular testing
- [x] Improve test for atlas component

## Day 65 - 02 Aug 2020 - Sun

- [x] Write test for `TrackMLComponent`
- [x] Improve test coverage of `TrackMLComponent` to 100%

## Day 66 - 03 Aug 2020 - Mon

- [x] Complete unit tests for `IOOptionsDialogComponent`
- [x] Improve `TrackMLComponent` tests
- [x] Complete unit tests for `ZoomControlsComponent`
- [x] Complete unit tests for `ObjectClippingComponent`

## Day 67 - 04 Aug 2020 - Tue

- [x] Complete unit tests for `ConfigSliderComponent`
- [x] Complete unit tests for `CollectionsInfoOverlayComponent`
- [x] Complete unit tests for `OverlayComponent`
- [x] Complete unit tests for `ObjectClippingComponent`
- [x] Fix warnings in tests by importing `AppModule` where required

## Day 68 - 05 Aug 2020 - Wed

- [x] Complete unit tests for `TreeMenuItemComponent`
- [x] Complete unit tests for `AutoRotateComponent`
- [x] Complete unit tests for `MainViewToggleComponent`
- [x] Complete unit tests for `ObjectSelectionComponent`
- [x] Complete unit tests for `IoOptionsComponent`
- [x] Complete unit tests for `InfoPanelComponent`
- [x] Complete unit tests for `EventSelectorComponent`
- [x] Complete unit tests for `DarkThemeComponent`
- [x] Complete unit tests for `CollectionsInfoComponent`

## Day 69 - 06 Aug 2020 - Thu

- [x] Fix async behavior of script loader
- [x] Complete unit tests for `PhoenixMenuNode`
- [x] Fix unit test of `CMSComponent`
- [x] Complete unit tests for `CMSLoader`
- [x] Exclude `src/services/extras` from coverage

## Day 70 - 07 Aug 2020 - Fri

- [x] Update jasmine, karma and testing related packages
- [x] Fix tests not passing after jasmine and karma updates
- [x] Complete unit tests for `ExperimentInfoComponent`
- [x] Complete unit tests for `JSRootEventLoader`
- [x] Add a sample root file to assets (for testing)

## Day 71 - 08 Aug 2020 - Sat

- [x] Complete unit tests for `InfoLoggerService`
- [x] Complete unit tests for `ThreeService`
- [x] Complete unit tests for `EventdisplayService`
- [x] Complete unit tests for `UIService`

## Day 72 - 09 Aug 2020 - Sun

- [ ] Weekend

## Day 73 - 10 Aug 2020 - Mon

- [x] Make an ig archive with less data for testing (to fix timeout errors for loading the archive)
- [x] Complete unit tests for `SceneManager`
- [x] Increase code coverage to 90%
- [x] Improve `ThreeService` tests

## Day 74 - 11 Aug 2020 - Tue

- [x] Keyboard controls for `UIService` operations
- [x] Keyboard controls for `ThreeService` operations
- [x] Keyboard controls for autorotate, zooming, clipping, switching views, toggling theme and preset views
- [x] Wait for discussions with mentor(s)

## Day 75 - 12 Aug 2020 - Wed

- [x] Use shift + "t" for toggling theme with keyboard
- [x] Wait for discussions with mentor(s) and shift work to weekend

## Day 76 - 13 Aug 2020 - Thu

- [x] Fix responsive behavior of Phoenix on mobile
- [x] Move experiment info to top right
- [x] Make phoenix menu responsive by changing styles
- [x] Fix experiment info styling for mobile devices and show experiment logo only

## Day 77 - 14 Aug 2020 - Fri

- [x] Fix UI menu not scrolling by touch on mobile devices (because of material tooltip)
- [x] Fix zoom hold on mobile devices
- [x] Make object selection better
- [x] Make object selection work on mobile devices (was not working before)

## Day 78 - 15 Aug 2020 - Sat

- [x] Start working on animations
- [x] Translate/tween the camera through the scene
- [x] Improve and modularize code for moving camera through the scene for animation

## Day 79 - 16 Aug 2020 - Sun

- [x] Make toggle for animating through the scene
- [x] Fix looping behavior of animating through the scene

## Day 80 - 17 Aug 2020 - Mon

- [x] Make camera animate toggle active only for animation duration and inactive when animation ends
- [x] Have a detailed talk with Edward
- [x] Start working on animating the event
- [x] Animate propagation of tracks in debugging

## Day 81 - 18 Aug 2020 - Tue

- [x] Use `BufferGeometry` for all phoenix objects (since it's better for performance)
- [x] Better animation for propagating tracks
- [x] Animation for scaling jets
- [x] Toggle for animating propagation of event objects

## Day 82 - 19 Aug 2020 - Wed

- [x] Close IO options dialog on loading an event
- [x] Fix bug of toggling visibility, changing color and other UI operations on geometry and event data with the same object name
- [x] Add animate event icon
- [x] Use scale and position to animate other event objects (hits and clusters)
- [x] Use buffer geometry for MuonChamber boxes

## Day 83 - 20 Aug 2020 - Thu

- [x] Add animation for collision of 2 particles
- [x] Start event animation after collision of 2 particles
- [x] Refactor code to make it consistent to use 2 spaces for tabs
- [x] Create an `AnimationsManager` for managing animation related operations and move all animation code there
- [x] Add an animation sphere to mock the propagation of event data for animation and make event data visible when the sphere reaches it

## Day 84 - 21 Aug 2020 - Fri

- [x] Edit hits geometry for animating hits to make only hits reached by the animation sphere visible on animation sphere tween update
- [x] Make hits params more readable
- [x] Create an extra tween for animating animation sphere beyond tracks
- [x] Analyze Tracer to check how they implement bloom

## Day 85 - 22 Aug 2020 - Sat

- [x] Create an `EffectsManager` for managing `EffectComposer` and all post processing passes
- [x] Move `OutlinePass` to `EffectsManager`
- [x] Try applying bloom to colliding particles (selective bloom doesn't work as expected and is not worth it)
- [x] Minor improvements to event animation
- [x] Analyze how Tracer animates events

## Day 86 - 23 Aug 2020 - Sun

- [x] Add function to animate event using clipping planes
- [x] Fix bugs with optional callbacks in animation functions and other improvements
- [x] Add support for animating event using clipping or using unique animations for different event data objects
- [x] Resolve conflicts for all open pull requests

## Day 87 - 24 Aug 2020 - Mon

- [x] Merge all open pull requests (HSF/phoenix#117, HSF/phoenix#118, HSF/phoenix#119, HSF/phoenix#120)
- [x] Fix major conflicts caused by merge pull requests
- [x] Fix failing tests because of the new elements
- [x] Fix overlay view not working
- [x] Start working on VR

## Day 88 - 25 Aug 2020 - Tue

- [x] Fix bug with Phoenix menu showing duplicating configs for detector
- [x] Apply better check to phoenix menu to see if the geometry folder already exists or not
- [x] Analyze how three.js `VRCreateButton` works
- [x] Create a custom VR button toggle for Phoenix which only shows on devices supporting VR
- [x] Debug problems with VR session initiation and get to a point where it works and shows a single plane (bugged)
- [x] Resolve conflicts for and merge PR for Runge-Kutta (HSF/phoenix#121)

## Day 89 - 26 Aug 2020 - Wed

- [x] Upgrade three.js to r120 and fix bugs introduced
- [x] Fix bugs with phoenix menu
- [x] Create a `VRManager` for managing VR operations and session
- [x] For VR - use a separate minimal animate loop and set it to the main renderer and clean it when exiting from VR
- [x] Support for initializing VR dedicatedly that is usable application wide

## Day 90 - 27 Aug 2020 - Thu

- [x] Fix bug with collection info selection icons (HSF/phoenix#128)
- [x] Improve the VR icon and fix the animate camera icon
- [ ] Try fixing some `.obj` geometries loading black with no material
- [x] Prepare for and present Phoenix in the ATLAS meeting
- [x] Add event display's `loadJSONGeometry` method to console `window` object
- [x] Make miscellaneous code improvements

## Day 91 - 28 Aug 2020 - Fri

- [x] Remove playground VR and use dynamic year for HomeComponent
- [x] Ability to end the VR session from the VR button
- [x] Set up VR camera group to use the camera in VR mode
- [x] Improve and optimize VR code
- [x] Use a cloned camera for VR to safely make changes to it
- [x] Add working controls for VR with ability to move in the headset direction or in the controller direction using the controller

## Day 92 - 29 Aug 2020 - Sat

- [x] Prepare GSoC report
- [x] Fix tests after updates to VR code
- [x] Create basic tests for `AnimationsManager`
- [x] Get Travis CI to work

## Day 93 - 30 Aug 2020 - Sun

- [x] Upgrade to Angular 10
- [x] Upgrade all npm packages to their latest versions and fix bugs introduced
- [x] Create a demo video for Phoenix
- [x] Update GSoC report

## Day 94 - 31 Aug 2020 - Mon

- [x] Create and add cover photo to link video in README
- [x] Fix API docs generation by using absolute links in README
- [x] Deploy the application
- [x] Refactor `RungeKutta` code
- [x] Create helper functions for extrapolating single or collections of tracks through `RungeKutta`
- [x] Re-add scale option to Detector in phoenix menu
