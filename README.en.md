# WKCoop: co-op for White Knuckle

[Русский](README.md) | **English**

An unofficial mod that turns White Knuckle into a co-op game for 2–4 players.

## Requirements

- **A licensed Steam copy of White Knuckle for every player.** The mod contains no game files and does not work without the game.
- Windows 10 or 11
- The same game and mod versions for all players, otherwise the host refuses the connection.

Tested on the game build with Unity 6000.3.9f1. A game update may break the mod.

## Installation

Every player needs to do this:

1. Download [WKCoop-Setup-0.4.9.exe](https://github.com/HBMFOB/WK-Coop/raw/main/WKCoop-Setup-0.4.9.exe).
2. Run it and press Install. The installer finds the game in your Steam libraries and installs the mod together with BepInEx 5.4.23.6. If the game is not found, choose its folder manually.

The file is not signed, so Windows SmartScreen may warn about an unknown publisher. If it does, press More info → Run anyway.

The installer and the F9 mod window each have a language button. Both start in Russian on a Russian system and in English otherwise.

**Updating:** run the installer of the new version.

**Uninstalling:** run the installer and press Remove the mod. The Remove BepInEx too checkbox fully restores the original game. It is a good idea to verify the game files in Steam after uninstalling.

## How to play

**Via Steam (recommended).** No port forwarding is needed: surprisingly, the game already includes all the required tools.

1. The host presses **F9** → Create a lobby and invite a friend, then picks a friend in the Steam overlay.
2. The friend accepts the Steam invite and connects automatically.
3. Everyone picks trinkets and difficulty modifiers (each player has their own) in the regular menu. A teammate presses I'm ready in the F9 window.
4. Once everyone is ready, the host presses Play.

**By IP** (LAN, Radmin VPN, Hamachi or forwarded TCP port 27877). Host: F9 → Start a server. Friend: F9 → enter the address → Connect.

At the moment only the main route and the first two shortcuts work properly. The game can be completed.

### Controls

| Key | Action |
|---|---|
| F9 | co-op window |
| Middle mouse button | place a marker everyone can see |
| Mouse and wheel (after death) | rotate the camera and change the distance |
| F10 (after death) | choose who to spectate |

## How co-op works

- **The world** is shared: the host picks the mode and the seeds are copied to the other players, so different game progress does not break anything.
- **Death.** A dead player becomes a spectator. Respawn comes after a host-defined delay and, by default, only while a living teammate is in a safe zone near vending machines. The run ends only when everyone is dead. If you get stuck (for example, your teammate moved on and closed the way behind them), the F9 window has a "Stuck: die and respawn next to a teammate" button.
- **Victory** is shared: when one player completes the game, the run is complete for everyone.
- **Buttons, levers, doors and transitions** work for everyone, but in some places they are still individual (the elevator, the barriers in the Nest). The terminal and separate rooms such as the roach shop are personal.
- **Items.** When one player picks up an item, it disappears for everyone. Each player has their own money, and a purchased item drops for everyone. Each player gets their own starter kit at the beginning of the Nest, freeze gun in Chimney and scanner at the Parasite entrance. The items of a player who disconnects drop where they stood.
- **Pistol.** Each player has their own pistol, and a hit on a teammate deals damage.
- **Sounds and light.** Teammates hear the sounds of your items and see your flares. A teammate's flashlight also shines from their bag if it is charged.
- **Skins.** A teammate's hands and held item show their own skin and palette.
- **Player models (experimental).** Instead of a capsule, a teammate can look like a 3D model: Harpy, Carrot, Miku or Teto. Each player picks their own: F9 → Your skin → Choose…. The models are built into the mod, and a teammate sees you as your model if they also run version 0.4.7 or newer. The models move on their own from what the player does: they walk, reach for handholds, hold items and wave their arms when falling, and Miku, Teto and Carrot change their facial expression.
- **Pause** is shared: if someone opens the pause menu, the world freezes for everyone.
- **Joining mid-run.** If the host allows it, a player who joins stays a spectator until the run ends. After that you should be able to play together.
- **Saves.** Disk saves are disabled in co-op: they are not needed, and they also partly changed the seeds, which caused desync. Every run starts fresh. Co-op runs are not sent to the Steam leaderboards.

## Settings

File: `BepInEx\config\com.wkcoop.whiteknuckle.cfg`. It appears after the first launch with the mod. Some settings can be changed in the F9 window.

| Setting | What it does |
|---|---|
| `Language` | interface language: `auto`, `ru` or `en` |
| `RespawnDelay` | respawn delay in seconds, 0 means no respawn |
| `RespawnOnlyInSafeRooms` | respawn only in safe zones |
| `MassFollowsLowestPlayer` | the Mass speeds up based on the lowest player |
| `GrabTeammates` | whether teammates can be grabbed |
| `SyncItems` | item synchronization |
| `SyncDenizens` | shared monsters controlled by the host |
| `RequireReady` | the host can start a run only after everyone confirms they are ready |
| `AllowJoinMidRun` | allow joining during a run as a spectator |
| `BlockLeaderboardsInCoop` | do not send co-op runs to the leaderboards |
| `MaxPlayers`, `Port`, `SendRate`, `MenuKey`, `ShowNameTags` | player limit, port, send rate, window key, name tags above players |
| `Skin` | your player model: `harpy`, `luuvan` (Carrot), `miku`, `teto`; empty means a capsule |

`RespawnDelay`, `RespawnOnlyInSafeRooms` and `SyncDenizens` come from the host and are sent to everyone when a run starts.

Launch options (Steam → Properties → Launch Options):

| Option | What it does |
|---|---|
| `-wkcoop-host` | start an IP server right away |
| `-wkcoop-connect 1.2.3.4[:port]` | connect by IP right away |
| `-wkcoop-name Name` | name for this session |
| `-wkcoop-lang en` | language for this session: `ru` or `en` |

## Known limitations

- The Parasite event is still being tested, and so are the challenges other than Roach Run.
- Items are not always picked up and dropped from the inventory correctly by other players, so they can be duplicated, or accidentally sold to the roach or ground up. This will not stop your progress and all items work, but it can spoil a run.
- Switching the shutters in the Nest kills the second player.
- In Body Cavity, key-locked doors get out of sync.
- Other players do not see the amalgamator at work.
- The perk for sacrificing an artifact is given to all players.
- If a player dies near the core, the game does not treat the floor in the finale as "safe" and does not respawn the dead.

If something does not work, check `BepInEx\LogOutput.log`: mod errors are written there.

## Feedback we would like

We have barely tested connection methods other than Steam, and we have not tested how many players the mod can handle, because only two of us own the game. These are the aspects we are most curious about. That does not make them the priority: polishing synchronization and making sure runs can be completed matters more to us. If you find bugs while playing as two, please report them too. We simply have almost no information about this part of the mod.

## License

The mod is distributed under the MIT License, see [LICENSE](LICENSE). The installer contains BepInEx and other third-party components, see [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

The mod is not affiliated with the developers of White Knuckle. All rights to the game belong to their respective owners.
