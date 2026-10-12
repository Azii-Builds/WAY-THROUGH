# WAY THROUGH

**Find your route. Build your loadout. Fight your way through.**

Created and developed by **Azaan**. Current documentation: **October 12, 2026**.

WAY THROUGH is a solo first-person shooter built in Unity. It combines illustrated environments, customizable weapons, tactical movement and six special abilities across an objective-based campaign, standalone districts and a zombie survival theater. Fight through guarded spaces, activate mission terminals and reach extraction—or see how many rounds you can survive in **The Last Screening**.

For a ready-to-use game overview, see [Game description](WayThrough-Unity/GAME-DESCRIPTION.md).

## Start playing

1. Open the Mac app, or install the Android test APK on a compatible device.
2. Select **Start Campaign**, **MAPS / WEAPON SELECTION**, or **ZOMBIES / THE LAST SCREENING**.
3. For a solo mission, choose a map and starting weapon, then select **DEPLOY**. Saved attachments apply to your selected weapon.
4. Follow the objective marker, use **F** at the mission terminal, and reach the exit. On mobile, use the **USE** button.

Zombie survival starts with the Colt 1911; buy other weapons during the match.

### Available packages

| Package | What it contains |
| --- | --- |
| `Way-Through-Mac.zip` | Standalone Mac game; extract and open `Way Through.app` |
| `Way-Through-Android.apk` | Android test build for ARM64 devices running Android 8.0 or later |
| `Way-Through-iOS-Xcode.zip` | iOS 15.0+ Xcode project; requires Xcode and Apple signing to install |
| `Way-Through-Unity-Project.zip` | Editable Unity project, source assets, documentation and validation results |

These are separate downloads. The source archive excludes generated builds and Unity's local cache. A local development checkout may also contain builds under `Builds/`.

The Mac app is a local build without commercial notarization. Android uses a development signing key. The iOS download is an Xcode export, not an installable IPA. See [Mobile setup](WayThrough-Unity/MOBILE-READ-ME.md) for installation details and testing limits.

## Modes and maps

### Campaign

The four-level campaign follows **The Compound → Freight District → Relay Fortress → The Foundry**. Each sector has an introductory sequence, armed encounters, a control objective and a gated exit. The Foundry adds furnace halls, elevated service catwalks, ramps and a cross-hall bridge.

Complete the objective before extracting. The pause menu includes a mission map. Campaign progress lasts for the current session; there is no save-slot system.

### District deployment

Choose **Skyline Market**, **Floodline**, **Signal Garden**, or **The Foundry** from **MAPS / WEAPON SELECTION**. The first three are standalone missions with encounters, supply points, a terminal and an extraction route. Compound, Freight, Relay and Zombies are also accessible from the deployment screen.

### The Last Screening

Survive escalating zombie rounds in an abandoned theater with stage access, dressing rooms, a film archive, an infirmary and a rear generator area. Earn points through hits and kills, open new areas, restore power, and purchase weapons, ammunition, perks and damage upgrades.

Shamblers arrive first, faster Stalkers join from round two, and tougher Brutes appear from round three. Temporary drops include max ammo, double points and instant kill. Your best round is saved separately from campaign scores.

The current game is **offline single-player**. Public matchmaking, multiplayer TDM and co-op are not implemented.

## Combat and customization

- **28 weapons** across assault, SMG, LMG, marksman, sidearm and shotgun categories. The arsenal uses seven base weapon/hand platforms with tuned variants.
- **31 non-stock attachment choices across nine slots**, including optics, muzzles, grips, barrels, magazines, stocks, lasers, ammunition and rear grips. Attachments change combat statistics; each weapon's saved build is independent.
- **Tactical movement:** sprint, crouch, jump and slide, with stamina costs and recovery.
- **Animated handling:** articulated support fingers, magazine exchanges, slide/bolt actions and individual shotgun shell insertion. Empty and partial reloads differ.
- **Recorded audio:** 24 firearm-handling cues and 12 gunfire clips, including quieter suppressor edits. Automatic shots overlap; enemy gunfire is directional.
- **Eight armed enemy roles:** Lookout, Bulwark, Runner, Jammer, Warden, Mender, Breacher and Marksman. Their abilities include armor, fast pursuit, ally alerts, healing and telegraphed precision shots.

Gunfire recordings are shared and adapted by weapon family; they are not individual recordings of all 28 models. Suppressed sounds are processed versions of the recordings. Sources and licenses are documented in [Audio credits](WayThrough-Unity/AUDIO-CREDITS.md).

## Abilities and pickups

Press **E** to cycle abilities and **Q** to activate the selected ability. Each has its own cooldown, shown on the HUD.

| Ability | Effect | Duration | Cooldown |
| --- | --- | --- | --- |
| Blink Step | Dash up to eight metres; solid cover stops the dash | Instant | 8 seconds |
| Gravity Lift | Launch upward with reduced gravity | 3 seconds | 18 seconds |
| Echo Decoy | Draw nearby enemies toward a hologram | 6 seconds | 24 seconds |
| Pulse Guard | Reduce incoming damage by 55% | 4 seconds | 20 seconds |
| Magnet Hand | Pull nearby unobstructed supplies and zombie drops toward you | Instant | 12 seconds |
| Time Pocket | Slow nearby enemies and hostile projectiles inside a local field | 6 seconds | 30 seconds |

Cooldowns pause with the game and reset on a new mission. Field supply pickups restore health, refill reserve ammunition or briefly increase movement speed; they display a respawn countdown after collection.

## Controls

| Input | Action |
| --- | --- |
| WASD | Move |
| Mouse | Look |
| Left mouse button | Fire; sidearms and marksman rifles fire once per click |
| Right mouse button | Aim |
| Left Shift + movement | Sprint |
| Space | Jump; skip a mission introduction |
| Left Ctrl or C | Crouch; press while sprinting to slide |
| R | Reload |
| F | Interact with doors, terminals, weapons, ammunition and survival machines |
| E | Cycle ability |
| Q | Activate selected ability |
| V | Switch Classic / Neo visual style |
| Escape | Pause / resume; skip a mission introduction |

On iOS and Android, touch controls appear automatically: move with the left stick, drag the right side to look, and use the on-screen action buttons. Movement, looking and firing support separate simultaneous touches. A desktop touch-preview toggle is available in the deployment screen.

## Visual style and settings

**Neo** uses rose concrete, sage/mint accents, graphite metal, illustrated contours and warm industrial lighting. **Classic** provides a monochrome presentation. The HUD displays health, stamina, ammunition, objectives and ability cooldowns, with weapon icons based on the equipped model and attachments.

Settings include graphics quality, resolution, sensitivity, audio levels and screen shake. Turning off screen shake disables reload camera motion. Settings, saved weapon builds and best scores persist locally.

Maps and characters are playable adaptations of the concept artwork. Some scenery is decorative: Foundry furnace glow does not deal damage, Floodline water is shallow, and Skyline cable cars are scenery. The separate Blender crew prototypes are not a playable character-selection system.

## Open the editable Unity project

1. Extract `Way-Through-Unity-Project.zip` if using the source download.
2. In Unity Hub, choose **Add → Add project from disk** and select the `WayThrough-Unity` folder.
3. Open with **Unity 6000.6.2f1**, the version recorded in `ProjectSettings/ProjectVersion.txt`.
4. Open `Assets/WayThrough/Scenes/WayThrough.unity` and press **Play**.

The scene contains a bootstrap that creates the world at runtime. Inspect generated objects during Play; edit the C# world generators or source assets for changes that persist after Play stops. The game and its bundled assets do not need a multiplayer account or a paid asset pack to run.

### Build from Unity

Install the appropriate platform support module in Unity Hub, then use:

| Unity menu | Output |
| --- | --- |
| **Way Through → Build macOS App** | `Builds/macOS/Way Through.app` |
| **Way Through → Build Android APK** | `Builds/Android/Way-Through.apk` |
| **Way Through → Export iOS Xcode Project** | `Builds/iOS/` |

The Mac build regenerates the stylized weapon assets and bootstrap scene. Mobile builds recreate the bootstrap scene and use the bundled weapon assets. Keep lasting changes in the authoring sources, and back up direct edits to generated assets before rebuilding.

### Project guide

| Location | Purpose |
| --- | --- |
| `Assets/WayThrough/Scripts/` | Gameplay, AI, maps, HUD, powers, audio and runtime checks |
| `Assets/WayThrough/Editor/` | Weapon/hand authoring tools, scene creation and platform builds |
| `Assets/WayThrough/Resources/` | Runtime models, shaders, UI art and recorded audio |
| `SourceModels/` | Preserved model sources and references |
| `SourceAudio/` | Recorded sound sources and provenance snapshots |
| `Tools/` | Asset preparation and inspection scripts |
| `Screenshots/` | Captures, motion previews and sound audition files |
| `TestResults/` | Saved checks and validation reports |

To make changes, keep the existing gameplay and asset credits intact, edit the relevant authoring source, and verify the affected feature in Play mode and a platform build. Add a focused runtime check when changing gameplay behavior.

## Validation and current limits

The recorded-audio update passed **158 gunfire runtime checks** and **581 reload regression checks**. An offline audio test exercised 12,000 shots across the 12 sound banks without clipping in those tested sequences. macOS and Android builds and the iOS export succeeded. Details: [Audio validation report](WayThrough-Unity/TestResults/recorded-gunfire-validation.json).

Earlier checks cover map routes, objectives, powers, touch ownership, enemy roles and zombie survival. Reports document their scope; automated traversal checks do not establish combat difficulty or a guaranteed frame rate.

Physical Android/iPhone testing is still pending. iOS signing and App Store/TestFlight distribution are not configured. Multiplayer remains deferred. No claim is made that the project reproduces a commercial game's assets or every detail in the concept art.

## Credits and further reading

- **Creator:** Azaan Ahmad
- [Game description](WayThrough-Unity/GAME-DESCRIPTION.md)
- [Mobile setup and limitations](WayThrough-Unity/MOBILE-READ-ME.md)
- [Audio sources and licenses](WayThrough-Unity/AUDIO-CREDITS.md)
- [Model credits](WayThrough-Unity/MODEL-CREDITS.md)
- [Archived development history](WayThrough-Unity/DEVELOPMENT-HISTORY.md) — older revision notes, including superseded details.

Third-party asset permissions are documented in the credit files; those licenses do not automatically license the entire game or its source code.
