# Agentic Gameplay Camera: playable demo (0.3.0)

A playable Windows demo of **Agentic Gameplay Camera 0.3.0**, the version on Fab:
https://www.fab.com/listings/6b94b623-7e95-4ac8-934e-0acea21f9ce0

It is a Development build of the plugin's sample gallery: one level of fourteen rooms, each
showing a camera mode, a state or a modifier on a playable character. The characters,
animation and level blocks come from Epic's Game Animation Sample.

## Download and run

1. Download `AgenticGameplayCamera_Demo_0.3.0_Win64.zip` from the
   [latest release](../../releases/latest) and unzip it anywhere.
2. Run `AgenticGameplayCamera_Demo_0.3.0\GameAnimationSample_5_8.exe`.

Windows 10 or 11, 64-bit, with a DirectX 12 graphics card. The exe is not code-signed, so
Windows SmartScreen may ask before the first run (More info, then Run anyway).

Move with the keyboard and mouse or a gamepad; the controls are the Game Animation Sample's.
Walk through a door and the room's camera takes over. Each room has a plaque on its back wall
saying what it shows and what to try, and the HUD at the top left shows the mode the camera is
running, the states the character is sending, and the live arm, FOV and lag numbers.

## The rooms

| # | Room | What it shows |
|--:|---|---|
| 01 | Exploration | The default third-person rig: sprint lane, slope, ledge, crouch tunnel |
| 02 | Combat.Melee | A closer arm, a pitch clamp of ±60, Awareness of two dummies, Focus |
| 03 | Combat.Ranged | A longer shoulder: arm 250 to 450 |
| 04 | Combat.Lockon | A clamp of −60/+45 with three dummies in an arc |
| 05 | Aim.Bow | A tight aim: FOV 60 to 75, clamp ±75 |
| 06 | Traversal yard | Vaults, a mantle, a drop, 10/20/30° ramps, a crouch rail, a tight corridor and an occluder wall |
| 07 | The cut | Crossing a line blends Exploration into Melee and back |
| 08 | The Standoff | An empty room in this version |
| 09 | The wall | An alcove with its back wall 120 cm behind you: the camera is pushed in, and looking up slides it down the wall |
| 10 | Slopes | Pitch Follow on three ramps |
| 11 | The lateral run | Yaw Follow round a pillar |
| 12 | Giants and dwarves | Targets that ask for their own arm and FOV |
| 13 | Targeting | Lock, cycle, target death and re-lock |
| 14 | Ragdoll yard | The camera holding a target through physics |

Room 13 uses **Agentic Targeting**, a separate plugin on Fab. It is included in this build;
the camera works without it, and in your own project that room needs it.

The console (`~`) also runs the gallery's own self-check, `AgenticCameraShowcase.RunAll`, which
teleports the character from room to room. In room 10 it stands the character inside the 20°
ramp, so the picture goes dark with the character in silhouette. Walking into room 10 never
does this, and the 0.4.0 gallery moves that spot onto the open floor beside the ramps.

## What it is not

The gallery is built for the editor and Development builds; it is not the shipping part of the
plugin. This repository holds this README and the release download only: no source, no plugin
files and no project.

## Files

| File | Size | SHA-256 |
|---|---|---|
| `AgenticGameplayCamera_Demo_0.3.0_Win64.zip` | 1,323,731,868 bytes (1.23 GiB) | `c824ed26ef87e2b33fcef90457efe9273ea37a0d44810ae0f4fc4ffe311eccb4` |

The `.sha256` file on the release holds the same hash. In PowerShell:
`Get-FileHash AgenticGameplayCamera_Demo_0.3.0_Win64.zip -Algorithm SHA256`.
