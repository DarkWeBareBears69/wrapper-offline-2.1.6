<div class="head" align="center">
  <h1>Wrapper: Offline ("2.1.6")</h1>
  <p><b>This project is not affiliated with or endorsed by GoAnimate Inc. or its product Vyond. Wrapper: Offline is a decentralized open-source initiative developed exclusively for archival purposes. It operates on a non-profit basis and does not accept any form of donations</b></p>
  <br>
</div>

Wrapper: Offline is a program designed to provide readily obtainable, irrevocable access to GoAnimate's retired assets in the modern era. It achieves this by replicating the original API and asset servers entirely on the computers of the users, while providing a simplistic frontend to interact with them. This project is important for archival purposes, as the ability to use the legacy GoAnimate editor and themes would be far trickier without it

This is an unofficial fork of GTAManRCRX's "2.1.4" release (itself a fork of the official release of W:O 2.1.0, created to fix serious long-standing bugs, consolidate dependencies, and improve portability), created to make additional improvements to 2.1.4, and reverse some controversial changes made by them.

## Changes
### Changes made since "2.1.4"
 - Restore the "Mosaic" props that were controversially removed by GTAMaxRCRX (commit [3110e61](https://github.com/DarkWeBareBears69/wrapper-offline-2.1.6/commit/3110e615c59c82db682615b7869d8a3f4d284b30)).
 - Add missing stock characters (commit [40acf38](https://github.com/DarkWeBareBears69/wrapper-offline-2.1.6/commit/40acf38c8ec87984b261527e48c7c707bb113e24))
 - Revert changes to capitalization made by GTAManRCRX.
### Dependencies
- Rewrite code dependent on Sharp to use FFmpeg instead, allowing W:O to natively run on Windows 7.
- Separated temp and userdata from the user's roaming AppData directory. User data is now stored in W:O's reaource directory.
- Nodezip was replaced with the more stable AdmZip to fix corruption issues.
- The build system can now automatically move the assets into the correct directory, set the icon for the W:O executable, and can package it for all supported platforms in a single run.
### Bug fixes
- Fixed the infamous Comedy World animation bug where the character's head would disappear or detach when selecting blow kiss or make fun of animations
- Fixed a bug where the scene would get stuck on "This character already has a voice" after creating a new scene
- Eliminated the redundant `resources/resources` folder structure that bloated the original build
- Fully restored character and video import functionality by fixing broken path logic in the source code
- Resolved issues with microphone recording
- Removed fake/misleading error messages that appeared during normal operation on the console
### Compatibility/Performance
- W:O can now run on 32-bit systems.
- Adobe Flash Player 32 has been upgraded to "Clean Flash" (a patched version of the still-maintained China-exclusive version of Flash Player).
- Removed large development packages like Mocha, Supertest, Nodemon, and Brotli to reduce package size and overhead.
- Updated FFprobe to version 2.1.1 to improve asset handling.
### Interface changes:
- Responsive settings panel with rounded corners that looks nice even on small screens
- Dark mode is now the default
- Removed the annoying flickering glitch of the sidebar
- Centered video titles, IDs, and dates
### User experience:
- Enhanced error handling for text-to-speech; removed broken/non-functional voice engines
- Readable dates: New format: Day [st/nd/rd/th] of Month YYYY - HH:MM:SS
- Locked video player aspect ratio: Disabled window resizing for the player to prevent Flash distortion and maintain pixel-perfect rendering, as Flash is not a responsive technology

## Downloads / Installation
**WARNING:** Wrapper: Offline 2.1.6 will make modifications to its AppData directory that will likely cause any custom characters or video projects to be deleted. Be sure to export these (or copy the directory to another location on your disk) before running 2.1.6.

To install Wrapper: Offline, you need to download it through the [releases page](https://github.com/DarkWeBareBears69/wrapper-offline-2.1.6/releases/)

### Updates And Support
For support, the first thing you should do is to [read through the Wrapper: Offline wiki](https://github.com/wrapper-offline/wrapper-offline/wiki), as it most likely has what you want to know    
Alternatively, if you can't find what you need, you can join the [Discord server](https://discord.gg/Kf7BzSw)
Joining the server is recommended, as there is a whole community that can help you out

### Building And Testing
To run Wrapper: Offline with a development server, first run this command
```
npm install
```
Then create a build
```
npm run build
```
And now you can run the development server with
```
npm run dev
```
### Packaging
To build a full copy of Wrapper: Offline
```
npm run package
```

### Contributions
If you have changes to the code that you want included, you can create a pull request [here](https://github.com/DarkWeBareBears69/wrapper-offline-2.1.6/pulls)

### A Disclosure On GoAnimate-Styled Rant Videos
Unlike GTAManRCRX's version 2.1.4, this version allows any rants and callouts on users; I'd prefer to have them made with this version rather than not allowing them at all. Even if it was trash. 

### License
Most of this project is free/libre software under the MIT license. You have the freedom to run, change, and share this as much as you want
FFmpeg is under the GNU GPLv2 license, which grants similar rights but has some differences from MIT. Flash Player (`resources/extensions`) and GoAnimate's original assets (`resources/static`) are proprietary and do not grant you these rights, but if they did, this project wouldn't need to exist

### To-Do
- [x] Restore the "Mosaic" props that GTAManRCRX removed

### Credits
| Contributor | Contribution |
| --------- | ------- |
| Benson | The original developer of Wrapper: Offline |
| DanielBitten | Upgraded TTS endpoints and voices |
| It'sJay | Saving every asset |
| MegaT | Eradicating the time bomb issue |
| Octanuary | The main developer. Rewriting the source code in Vue and TypeScript |
| VisualPlugin | The developer of the GoAnimate Wrapper |
| [Vyond](https://www.vyond.com) | The creators of GoAnimate |
| [Whispery](https://www.youtube.com/channel/UCVgwK9guSmcb3GkYLBzAbgA) | Fixing issues with Windows 11 and macOS |


[Whispery's Discord page](https://discord.com/users/1440498123997843607)

No members of the original GoAnimate wrapper team are officially working on Wrapper: Offline, even if they have contributed. Some members of the original team have asked not to be given credit, and they have been removed.

Credit also goes to GTAManRCRX (the creator of the "2.1.4" fork), and DarkWeBareBears69 (the creator of this fork).
