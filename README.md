> [!NOTE]
> #### To modify these flags on your Roblox client, you can install [Bloxstrap](https://github.com/pizzaboxer/bloxstrap). [Install here](https://github.com/pizzaboxer/bloxstrap/releases/latest), and install it. Then open Bloxstrap Menu.
> #### To modify these flags on your Roblox Studio client [Roblox Studio Mod Manager](https://github.com/MaximumADHD/Roblox-Studio-Mod-Manager). [Exe](https://github.com/MaximumADHD/Roblox-Studio-Mod-Manager/raw/main/RobloxStudioModManager.exe)/[Zip](https://github.com/MaximumADHD/Roblox-Studio-Mod-Manager/archive/main.zip) After installation, install Roblox studio and use Edit Flags to create overrides.
> ### Modifying your client without a third-party program (Modifications will not be saved across updates):
> 1. Find your Roblox Installation directory. Typically found at %localappdata%\Roblox\Versions\ for Windows.
> 2. Identify the folder starting with the name "version" containing RobloxPlayerBeta.exe for Roblox, or RobloxStudioBeta.exe for Roblox studio.
> 3. Create a folder inside the version folder and name it to "ClientSettings".
> 4. Add a txt file and rename it to "ClientAppSettings.json" and write {}, Example of a flag modification:
> ```
> {
>   DFIntConnectionMTUSize: 900,
>   FIntDebugForceMSAASamples: 4,
>   UserRaycastPeformanceImprovements: "true",
> }

# Performance user flags

## Client-sided
- `UserRaycastPeformanceImprovements`
   - Uses ```workspace:Raycast()``` instead of ```worldmodel:FindPartOnRayWithIgnoreList()```
 - `UserUpdateInputConnections`
   - Disconnects unrequired connections, better memory usage
## Micro-optimizations
**Networking**
- `DFIntConnectionMTUSize <number> <range(900, 2500+)>`
  - Recommended: `900`
- `DFIntOptimizePingThreshold: <number> <range(50ms, 200ms+)>`
  - Recommended: 50ms
- `FFlagEnableQuickGameLaunch <boolean>`
  - May improve load times, slightly **buggy.**

# Rendering engine
- `FIntDebugForceMSAASamples <number> <range(0x, 4x)>`
  - Any value over 4x will break viewport-frames.

- `FIntRenderLocalLightUpdatesMax <number>`
- `FIntRenderLocalLightUpdatesMin <number>`
   - A range limit to light-updates, lower values in games with Future lighting may improve peformance but cause artifacting.
}

# Optional features
- `UserCameraToggle <boolean>`

# Recommended, probably Default
- `UserCameraInputDt <boolean>`
  - Makes camera movement relative to real-time instead of to framerate.

# General
 - `UserHideCharacterParticlesInFirstPerson <boolean>`
   - Hides particles in first person
# Sounds
 - `UserSoundsUseRelativeVelocity2 <boolean>`, `UserSoundsUseRelativeVelocity <boolean>`
   - Sounds act as if they are in Unity when they are in a part that is moving. (High pitch when moving, normal pitch when normal velocity)
# Gamepad
 - `UserFixGamepadMaxZoom <boolean>`
   - Stops zoom controller if zoom has reached the maximum zoom, reseting it back to the minimum.
 - `UserFixGamepadSensitivity <boolean>`
   - Makes gamepad camera control affected by [sensitivity](<https://create.roblox.com/docs/reference/engine/classes/UserGameSettings#GamepadCameraSensitivity>).
# Virutal Reality
  - `UserVRVehicleCamera2 <boolean>`
    - Makes the VR camera in Third person move with the vehicle the character is in.
# Unremarkable
## Touch screens
  - `UserClearPanOnCameraDisable <boolean>`
    - Clears the touch-screen's panning
  - `UserResetTouchStateOnMenuOpen <boolean>`
    - Resets all touch data when opening the Roblox ESC menu.
  - `UserDynamicThumbstickSafeAreaUpdate <boolean>`
    - Changes safe-area for where the thumbstick is.
  - `UserClampClassicThumbstick <boolean>`
    - Uses a older version of the thumbstick controls.
  - `UserFixTouchJumpBug2 <boolean>`
    - Briefly de-activate the jump controller when the input for it is reconnected.
  - `UserDynamicThumbstickMoveOverButtons <boolean>`
    - Uses ```UserInputService.TouchMoved``` over ```ContextActionService``` when using the thumbstick.
## Click to move
   - `UserExcludeNonCollidableForPathfinding <boolean>`
     - Changes Width and Height for Pathfinding parameters based on Character extents.
   - `UserClickToMoveSupportAgentCanClimb2 <boolean>`
     - Enable character to climb Trusses using Click to move.
## Builtin freecam
   - `UserExitFreecamBreaksWithShiftlock <boolean>`
     - Exiting the freecam while Shift lock is enabled causes a bug to happen, when this flag is enabled, the bug is solved.
   - `UserShowGuiHideToggles <boolean>`
     - Hides UI during freecam
## Animate script
   - `UserNoUpdateOnLoop <boolean>`
     - Animations that are not looped with be automatically looped by setting the time-position to 0 when the animation ends.
   - `UserAnimateScaleRun <boolean>`
      - Taller characters have a slower walking animation.
## Bug fixes
- `UserFixCameraOffsetJitter2 <boolean>`
