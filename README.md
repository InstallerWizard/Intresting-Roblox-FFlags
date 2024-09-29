# Intresting-Roblox-FFlags
Roblox FFlags and User flags of my picking

# * Performance user flags
- `UserRaycastPeformanceImprovements`
  - Uses ```workspace:Raycast()``` instead of ```worldmodel:FindPartOnRayWithIgnoreList()```
 - `UserUpdateInputConnections`
  - Disconnects unrequired connections, better memory usage

# * Optional features
- `UserCameraToggle`

# * Recommended, probably Default
- `UserCameraInputDt`
  - Makes camera movement relative to real-time instead of to framerate.

# * General
 - `UserHideCharacterParticlesInFirstPerson`
   - Hides particles in first person
# * Sounds
 - `UserSoundsUseRelativeVelocity2`
   - Sounds act as if they are in Unity when they are in a part that is moving. (High pitch when moving, normal pitch when normal velocity)
# * Gamepad
 - `UserFixGamepadMaxZoom`
   - Stops zoom controller if zoom has reached the maximum zoom, reseting it back to the minimum.
 - `UserFixGamepadSensitivity`
   - Makes gamepad camera control affected by [sensitivity](<https://create.roblox.com/docs/reference/engine/classes/UserGameSettings#GamepadCameraSensitivity>).
# * Virutal Reality
  - `UserVRVehicleCamera2`
    - Makes the VR camera in Third person move with the vehicle the character is in.
# * Unremarkable
## + Touch screens
  - `UserClearPanOnCameraDisable`
    - Clears the touch-screen's panning
  - `UserResetTouchStateOnMenuOpen`
    - Resets all touch data when opening the Roblox ESC menu.
  - `UserDynamicThumbstickSafeAreaUpdate`
    - Changes safe-area for where the thumbstick is.
  - `UserClampClassicThumbstick`
    - Uses a older version of the thumbstick controls.
  - `UserFixTouchJumpBug2`
    - Briefly de-activate the jump controller when the input for it is reconnected.
  - `UserDynamicThumbstickMoveOverButtons`
    - Uses ```UserInputService.TouchMoved``` over ```ContextActionService``` when using the thumbstick.
## + Click to move
   - `UserExcludeNonCollidableForPathfinding`
     - Changes Width and Height for Pathfinding parameters based on Character extents.
   - `UserClickToMoveSupportAgentCanClimb2`
     - Enable character to climb Trusses using Click to move.
## + Builtin freecam
   - `UserExitFreecamBreaksWithShiftlock`
     - Exiting the freecam while Shift lock is enabled causes a bug to happen, when this flag is enabled, the bug is solved.
   - `UserShowGuiHideToggles`
     - Hides UI during freecam
## + Animate script
   - `UserNoUpdateOnLoop`
     - Animations that are not looped with be automatically looped by setting the time-position to 0 when the animation ends.
   - `UserAnimateScaleRun`
      - Taller characters have a slower walking animation.
## + Bug fixes
- `UserFixCameraOffsetJitter2`

-# By <@612204453541576704>, MadnessMyth
