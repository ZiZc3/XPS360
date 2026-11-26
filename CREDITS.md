# XPS360 credits and licences

**Developer: AZiZ**

XPS360 is an Xbox 360 emulator for PS5, built on Xenia Edge.

| Project | Licence | What XPS360 uses it for |
|---|---|---|
| Xenia | BSD 3-Clause | the Xbox 360 emulator this app is built on |
| Xenia Edge | BSD 3-Clause | the Xenia fork XPS360 builds on |
| Xenia Canary game patches ([xenia-canary/game-patches](https://github.com/xenia-canary/game-patches), commit 89b08ee) | no licence file in the repository; each patch is credited to its authors (its `author` line) | the community game patches in Game Options > Patches: 505 files, 1769 patches, 324 titles, compiled in unchanged (as Xenia Edge's own builds ship them), every one off until the user turns it on for a game |
| Selawik 1.01 (Microsoft) | SIL OFL 1.1 | the dashboard font, baked as "XPS360 UI Sans" (OFL text ships in the app) |
| DejaVu Sans | Bitstream Vera licence / public domain | symbols, arrows, Greek and Cyrillic in the dashboard font |
| Fluent UI System Icons (Microsoft) | MIT | dashboard tile and menu icons |
| Kenney Input Prompts 1.5A | CC0 | PlayStation button symbols |
| webos-nxe | MIT | NXE orb ring timing values (ripples) |
| ProsperoEden (BlackBearReloaded) | GPL-3.0-or-later | DualSense HD haptics (dashboard ticks and games' rumble on the pad's vibration audio port), via XPSemu's haptics_ps5.c |
| MihawkGen (PS5_MihawkGen, Mihawk) | GPL-3.0-or-later | frame generation: a game at a steady 30 fps shown at 60 (neural interpolator, colour only, weights compiled in), via XPSemu; source and licence in `src/xenia/ui/vulkan/mihawkgen/` |
| PS5SX2 (Swordpdf) | GPL-3.0 | PS5 trophy notifications (Settings > Launcher > Achievement style: PS5 trophies): the system-notification relay payload (`tools/notify/xps360_notify.c`, from `ps5/coreorbis/notify-relay/notify_relay.c`), the toast's JSON layout, sound ids and pacing (`xui360/notify.cc`, from `ProsperoNotify.cpp`). The trophy tier pictures and sounds are the console's own, read on the console, never copied into the app |
| OrthoDad38 NXE launcher | MIT | cover-flow ideas |
| msdf-atlas-gen (Viktor Chlumsky) | MIT | font atlas baking (build tool, not shipped) |
| Mbed TLS | Apache-2.0 | HTTPS for the System Update download |
| Mozilla CA certificate bundle | MPL-2.0 | trusted root certificates |
| FFmpeg | LGPL-2.1-or-later | XMA audio decoding |
| Mesa RADV | MIT | the Vulkan driver |
| LLVM | Apache-2.0 WITH LLVM-exception | native CPU code (way 3) |
| AMD FidelityFX CAS / FSR 1 | MIT | CAS sharpening of the game's picture (our own code of ffx_cas.h's no-scaling path, via XPSemu's swapchain.c) and FSR 1 upscaling (EASU + RCAS, Xenia's presenter) |
| SMAA (Jorge Jimenez, Jose I. Echevarria, Belen Masia, Fernando Navarro, Diego Gutierrez) | MIT | SMAA 1x anti-aliasing, as ported to XPSemu; SMAA.hlsl + area / search textures from iryoku/smaa 71c806a in `src/xenia/gpu/shaders/xps360_smaa.hlsli` and `src/xenia/gpu/vulkan/xps360_smaa_*.h` |
| NVIDIA FXAA 3.11 (Timothy Lottes) | BSD 3-Clause | FXAA anti-aliasing (Xenia's pass, tuned as XPSemu's: edges only); `third_party/fxaa` |
| Vulkan Memory Allocator (AMD) | MIT | GPU memory |
| glslang / SPIRV-Tools / SPIRV-Headers (Khronos) | BSD-3 / Apache-2.0 | shader translation |
| Dear ImGui | MIT | debug panels and the classic launcher |
| {fmt} | MIT | text formatting |
| toml++ | MIT | settings files |
| stb_image / stb_image_write / stb_truetype | Public domain / MIT | pictures |
| xxHash | BSD 2-Clause | hashes |
| zlib-ng | zlib | compression |
| Zstandard | BSD | compression |
| Snappy | BSD 3-Clause | compression |
| libmspack | LGPL-2.1 | LZX decompression |
| Xbyak | BSD 3-Clause | x86-64 code generation |
| Capstone | BSD 3-Clause | disassembly |
| pugixml | MIT | XML (game details) |
| utfcpp | BSL-1.0 | UTF-8 text |
| half | MIT | 16-bit floats |
| date (Howard Hinnant) | MIT | dates |
| disruptorplus | MIT | queues |
| cxxopts | MIT | options |
| ps5-payload-sdk (John Törnblom) | GPL-3.0 with exceptions | PS5 toolchain and headers |
| XPSemu | GPL-2.0 (xemu) | our original Xbox emulator for PS5: haptics, adaptive trigger presets, launcher ideas |
| Droid Sans Fallback (Google) | Apache-2.0 | the Japanese and Chinese language names in the dashboard font |
| Noto Sans KR (Google) | SIL OFL 1.1 | the Korean language name in the dashboard font |
| Aurora JTAG/RGH Trainer Pack Repository ([StonedModder](https://github.com/StonedModder/Aurora-JTAG-RGH-Trainer-Pack-Repository)) | each trainer by its authors | the trainers in Game Options > Cheats: downloaded on the console from the repository when you ask for them, never shipped in the app |
| ReXGlue SDK (Tom Clay) | BSD 3-Clause | its code generator builds the per-game native CPU modules (XPS360 Native) |
| XenDroid (rfandango) | BSD 3-Clause (Xenia) | POSIX core fixes and per-game ideas (mid-frame submission, package handling) |
| gta4-ps5 | GPL-3.0 | ideas: holding a frame before present, the GPU memory recycler (rewritten here) |
| XPS360 app icon ([digbaddyjack](https://www.reddit.com/r/xbox/comments/17012xf/i_made_custom_xbox_desktop_icons/)) | used with credit | the app's home screen icon (`sce_sys/icon0.png`) and the README logo |

## Not shipped

No Microsoft files are in the app or the source tree. The dashboard art, sounds and the
boot intro come from the user's own console system update (downloaded and unpacked on
the console); box art, backgrounds and game details come from Microsoft's public servers
and stay in the console's cache.
