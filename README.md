<p align="center">
  <img src="assets/xps360-logo.png" alt="XPS360" width="140">
</p>

<h1 align="center">XPS360</h1>

<p align="center">
  <strong>Xbox 360 games on a PlayStation 5.</strong><br>
</p>

<p align="center">
  <code>v1.0</code> &nbsp;&middot;&nbsp;
  <code>GPL-3.0</code>
</p>

---

## What is XPS360?

XPS360 is an Xbox 360 emulator for the PlayStation 5, running as a native app. It is built on **[Xenia Edge](https://github.com/has207/xenia-edge)**.

The Xbox 360 has a PowerPC CPU, so its code has to be translated. XPS360 **compiles each game's code into real PS5 code** and keeps it, so from the next launch on the game runs natively from its first frame. Graphics are drawn through Vulkan.

---

## Features

- Xbox 360 home screen in three styles: Metro, NXE and Blades
- Box art, game details, play time and Continue
- Achievements as PS5 trophies or Xbox 360 pop-ups
- In-game Guide, up to 4 profiles and 4 players
- DualSense HD haptics and adaptive triggers
- Anti-aliasing: FXAA, SMAA, CAS sharpening, FSR 1 upscaling
- Game patches (60 FPS, widescreen), cheats, DLC and title updates per game
  and much more.

---

## Install

You need a PS5 with **kstuff** running, and **[ShadowMountPlus](https://github.com/drakmor/ShadowMountPlus)**.

1. Copy `PPSA93442/` to `/data/homebrew/`.
2. Put your games in `/data/xps360/games/`, or use **Add Games** on the dashboard (USB drives works too).
3. Launch **XPS360** from the home screen.

---

## Building

**Toolchain:** PS5 payload SDK and RADV from [PS5_Vulkan](https://github.com/mihawk-99/PS5_Vulkan) (built first), on Linux or WSL, plus LLVM 18.

---

## Credits

- **[Xenia](https://github.com/xenia-project/xenia)** and **[Xenia Edge](https://github.com/has207/xenia-edge)**: the Xbox 360 emulator XPS360 is built on
- **[Xenia Canary game patches](https://github.com/xenia-canary/game-patches)**: the community game patches
- **[Aurora trainer pack](https://github.com/StonedModder/Aurora-JTAG-RGH-Trainer-Pack-Repository)** by StonedModder: cheats
- **[Mihawk-99](https://github.com/mihawk-99)**: [PS5_Vulkan](https://github.com/mihawk-99/PS5_Vulkan) (RADV on the PS5)
- **[PS5SX2](https://github.com/Swordpdf/PS5SX2)** by Swordpdf: PS5 trophy notifications
- **[ProsperoEden](https://github.com/heydemoura/ProsperoEden)** (BlackBearReloaded): DualSense HD haptics
- **[ReXGlue SDK](https://github.com/rexglue/rexglue-sdk)**, **[XenDroid](https://github.com/rfandango/XenDroid)** by rfandango and **[gta4-ps5](https://github.com/elripalda/gta4-ps5)** by elripalda: native code and core ideas
- **[ps5-payload-dev SDK](https://github.com/ps5-payload-dev/sdk)**, **[kstuff](https://github.com/EchoStretch/kstuff)**, **[ShadowMountPlus](https://github.com/drakmor/ShadowMountPlus)** and the PS5 scene
- **[LLVM](https://llvm.org)**, **[Mesa RADV](https://mesa3d.org)**, **[FFmpeg](https://ffmpeg.org)**, **[AMD FidelityFX](https://github.com/GPUOpen-Effects)**, **[SMAA](https://github.com/iryoku/smaa)**, **[Dear ImGui](https://github.com/ocornut/imgui)** and the other libraries in [CREDITS.md](CREDITS.md)
- App icon: by **[digbaddyjack](https://www.reddit.com/user/digbaddyjack/)**
- Icons: **[Fluent UI System Icons](https://github.com/microsoft/fluentui-system-icons)** (MIT), **[Kenney Input Prompts](https://kenney.nl/assets/input-prompts)** (CC0)
- **[XPSemu](https://github.com/ZiZc3/XPSemu)**: our original Xbox emulator for PS5

---

## License

GPL-3.0. Third-party parts keep their own licenses (see [CREDITS.md](CREDITS.md)).

XPS360 includes no Microsoft dashboard, system software, game or other Xbox 360 files. Use your own games, dumped from discs you own.
