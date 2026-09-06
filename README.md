<div class="head" align="center">
  <h1>Wrapper Offline</h1>
  <p><b>This project is not affiliated with or endorsed by GoAnimate Inc. or its product Vyond. Wrapper Offline is a decentralized open-source initiative developed exclusively for archival purposes. It operates on a non-profit basis and does not accept any form of donations</b></p>
  <br/>
</div>

Wrapper Offline is a software designed to provide readily obtainable, irrevocable access to GoAnimate's retired assets in the modern era    
It achieves this by replicating the original API and asset servers entirely on the computers of the users, while providing a simplistic frontend to interact with them
This project is important for archival purposes, as the ability to use the legacy GoAnimate editor and themes would be far trickier without it

### 🚀 Wrapper Offline 2.1.6
This version is a complete overhaul of the UI redesign prototype version of the 2.1.0 source code. Over 40+ critical bugs have been fixed, unnecessary dependencies removed, and the core packages swapped for maximum compatibility and portability
### 🛠️ Major Architectural Changes
- Sharp → FFmpeg Migration: Replaced the binary-heavy Sharp with FFmpeg, as that is a Wrapper offline dependency anyway. This enables 100% native Windows 7 support without needing VxKex or any kernel extensions
- Pure Portability: Separated temp and userdata from %APPDATA%. All data now stays within the program’s resources folder, leaving a zero footprint in your AppData folder
- Nodezip → AdmZip: Swapped the unreliable nodezip for AdmZip for stable ZIP compression and metadata handling
- Automated Build Process: Fully automated the build script that handles asset relocation, icon selection (ICO/PNG/ICNS), and multi-arch packaging in a single go
### 🐛 Critical Bugfixes (The "fixed" list)
- The "No Head" glitch with two female characters: Fixed the infamous Comedy World animation bug where the character's head would disappear or detach when selecting blow kiss or make fun of animations
- Cache Lock Fixed: Fixed a bug where the scene would get stuck on "This character already has a voice" after creating a new scene
- Resource Simplification: Eliminated the redundant `resources/resources` folder structure that bloated the original build
- Import Fixes: Fully restored character and video import functionality by fixing broken path logic in the source code
- Microphone Fix: Resolved issues with native microphone recording
- Ghost Errors Purged: Removed fake/misleading error messages that appeared during normal operation on the console
### 💻 Compatibility And Performance
- Native x86 Support: First-ever stable build for Windows x86 and Linux x86 architectures
- Flash 34 Integration: Upgraded to Clean Flash 34.0.0.118 (from 32.0.0.371) for better stability and performance
- Dependency Purge: Removed heavy and unnecessary dev tools like mocha, supertest, nodemon, and brotli to reduce package size and overhead
- FFprobe Upgrade: Updated from 1.4.1 to 2.1.1 for better asset handling
### UI Polish:
- Responsive settings panel with rounded corners that looks nice even on small screens
- Dark mode is now the default
- Removed the annoying flickering glitch of the sidebar
- Centered video titles, IDs, and dates
### 📝 User Experience (UX)
- Better TTS: Enhanced error handling for text-to-speech; removed broken/non-functional voice engines
- Readable dates: New format: Day [st/nd/rd/th] of Month YYYY - HH:MM:SS
- Locked video player aspect ratio: Disabled window resizing for the player to prevent Flash distortion and maintain pixel-perfect rendering, as Flash is not a responsive technology
### 💡 Why Choose THIS Version?
This version is built for longevity and stability. It runs on Windows 7 natively, consumes fewer resources, and fixes the most annoying bugs that occurred in the previous Wrapper offline versions

### ⚠️ Before You Move Or Test This Version...
You need to back up your Wrapper Offline 2.1.0 roaming data, since this version will mess up and delete everything in the roaming data. However, the custom assets are fine in your Wrapper Offline 2.1.0 build. Just the character and video data are affected.

### Downloads / Installation
To install Wrapper Offline, you need to download it through the [releases page](https://github.com/GTAManRCRX/wrapper-offline-fixed/releases/)

### Updates And Support
For support, the first thing you should do is to [read through the Wrapper offline wiki](https://github.com/wrapper-offline/wrapper-offline/wiki), as it most likely has what you want to know    
Alternatively, if you can't find what you need, you can join the [Discord server](https://discord.gg/Kf7BzSw)
Joining the server is recommended, as there is a whole community that can help you out

### Building And Testing
To run Wrapper Offline with a development server, first run this command
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
To build a full copy of Wrapper Offline
```
npm run package
```

### Pull Requests Are Allowed
Since I'm not a coder, you can fix it yourself and send a request.

### A Disclosure On GoAnimate-Styled Rant Videos
Unlike GTAManRCRX's version 2.1.4, this version allows any rants and callouts on users; I'd prefer to have them made with this version rather than not allowing them at all. Even if it was trash. 

### License
Most of this project is free/libre software under the MIT license. You have the freedom to run, change, and share this as much as you want
FFmpeg is under the GNU GPLv2 license, which grants similar rights but has some differences from MIT. Flash Player (`resources/extensions`) and GoAnimate's original assets (`resources/static`) are proprietary and do not grant you these rights, but if they did, this project wouldn't need to exist

### To-Do
- [x] Bringing The Mosaic Props Back

### Credits
| Contributor | Contribution |
| --------- | ------- |
| Benson | The original developer of Wrapper offline |
| DanielBitten | Upgraded TTS endpoints and voices |
| It'sJay | Saving every asset |
| MegaT | Eradicating the time bomb issue |
| Octanuary | The main developer. Rewriting the source code in Vue and TypeScript |
| VisualPlugin | The developer of the GoAnimate wrapper |
| [Vyond](https://www.vyond.com) | The creators of GoAnimate |
| [Whispery](https://www.youtube.com/channel/UCVgwK9guSmcb3GkYLBzAbgA) | Fixing issues with Windows 11 and macOS |


[Whispery's Discord page](https://discord.com/users/1440498123997843607)

No members of the original GoAnimate wrapper team are officially working on Wrapper offline, even if they have contributed. Some members of the original team have asked not to be given credit, and they have been removed
