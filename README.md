# Angel Aura Amethyst (iOS)
[![Development build](https://github.com/AngelAuraMC/Amethyst-iOS/actions/workflows/development.yml/badge.svg?branch=main)](https://github.com/AngelAuraMC/Amethyst-iOS/actions/workflows/development.yml)
[![Crowdin](https://badges.crowdin.net/angelauramc/localized.svg)](https://crowdin.com/project/angelauramc)
[![Discord](https://img.shields.io/discord/724163890803638273.svg?label=&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/5ptqkyZxEy)



## Introduction
Amethyst is a Minecraft: Java Edition launcher for Android, iOS, and iPadOS, based off of zhuowei's [Boardwalk](https://github.com/zhuowei/Boardwalk) project.
* Supports most versions of Minecraft: Java Edition, from the very first beta to the newest snapshots.
* Supports Forge, Fabric, OptiFine, and Quilt for you to customize the experience with supported mods.
* Includes customizable on-screen controls, keyboard and mouse support, and game controller support.
* Optimized for jailbroken and TrollStore devices to enable better capabilities.
* Microsoft account and demo mode support for logging into Minecraft.
* ...and much more!

This repository contains the code for our iOS and iPadOS port of Amethyst. Looking for [Android?](https://github.com/AngelAuraMC/Amethyst-Android)

## Getting started with Amethyst
The [Amethyst wiki](https://wiki.angelauramc.dev/wiki/getting_started/INSTALL.html#ios) has extensive documentation on how to install, set up, and play! For those who wish to install quickly, here's the basics:

### Requirements
At the minimum, you'll need one of the following devices on **iOS 14.0** and later:
- iPhone 6s and later
- iPad (5th generation) and later
- iPad Air (2nd generation) and later
- iPad mini (4th generation) and later
- iPad Pro (all models)
- iPod touch (7th generation)

However, we recommend one of the following devices on **iOS 14.0** and later:
- iPhone XS and later, excluding iPhone XR and iPhone SE (2nd generation)
- iPad (10th generation) and later
- iPad Air (4th generation) and later
- iPad mini (6th generation) and later
- iPad Pro (all models, except for 9.7-inch)

Recommended devices provide a smoother and more enjoyable gameplay experience compared to other supported devices.
- iOS 17.x and iOS 18.x is supported. However, a computer is required. For more information, please check out [the official wiki](https://wiki.angelauramc.dev/wiki/faq/ios/JIT.html#what-are-the-methods-to-enable-jit)

### Setting up to sideload
Amethyst can be sideloaded in many ways. Our recommended solution is to install [TrollStore](https://github.com/opa334/TrollStore) if your iOS version supports it. Installing with TrollStore allows you to permanently sign the application, automatically enable JIT, and increase memory limits.

If you cannot, [AltStore](https://altstore.io) and [SideStore](https://sidestore.io) are your next best options.
- Signing services that do not use your UDID (and use distribution certificates) are not supported, as Amethyst requires capabilities they do not allow. However, if you do managed to gain access to a Development certificate, due to it having the necessary entitlement (being com.apple.security.get-task-allow) to attach a debugger to the running process (enabling JIT), you may use a Development certificate.
  
- Only install sideloading software and Amethyst from trusted sources. We are not responsible for any harm caused by using unofficial software.
- Jailbreaks also benefit from permenant signing, autoJIT, and increased memory limits. However, we do not recommend them on devices intended for regular use.

### Installing Amethyst
#### Release build (TrollStore)
1. Download an IPA of Amethyst in [Releases](https://github.com/AngelAuraMC/Amethyst-iOS/releases).
2. Open the package in TrollStore using the share menu.

#### Release build (AltStore/SideStore trusted source)
These builds will be available soon, stay tuned.

#### Nightly builds
*These builds can contain game-breaking bugs. Use with caution.*
1. Download an IPA build of Amethyst in the [Actions tab](https://github.com/AngelAuraMC/Amethyst-iOS/actions).
2. Open the downloaded IPA in your sideloading app to install.

#### Nightly builds (AltStore/SideStore trusted sources)
These builds will be available soon, stay tuned.

### Enabling JIT
Amethyst makes use of **just-in-time compilation**, or JIT, to provide usable speeds for the end user. JIT is not supported on iOS without the application being debugged, so workarounds are required to enable it. You can use this chart to determine the best solution for you and your setup.
| Application         | AltStore | SideStore | StikDebug | TrollStore | Jitterbug          | Jailbroken |
|---------------------|----------|-----------|-----------|------------|--------------------|------------|
| Requires ext-device | Yes      | Yes (#)   | Yes (#)   | No         | If VPN unavailable | No         |
| Requires Wi-Fi      | Yes      | Yes (#)   | Yes (#)   | No         | Yes                | No         |
| Auto enabled        | Yes (*)  | No        | Yes       | Yes        | No                 | Yes        |

(*) AltServer running on the local network is required.
(#) Only the first time.

### Enabling Increased Memory Limit
In order for Amethyst to run even smoother, it's recommended to increase the RAM limit by enabling "Increased Memory Limit." You can enable it by installing [this](https://github.com/hugeBlack/GetMoreRam/releases/download/nightly/Entitlement.ipa) app with your favorite sideloading service. You will need to sign in with the Apple ID you used in AltStore/SideStore and press "Refresh" in the App-IDs tab. Choose the App-ID of Amethyst (or LiveContainer if you're using Amethyst in it) and press "Add Increased Memory Limit." After reinstalling Amethyst (or LiveContainer), you can see in the logs, or with tools like [Antrag](https://apps.apple.com/app/antrag/id6747074491), if Increased Memory Limit has been enabled successfully. If not, try again.

## Contributors
Amethyst is amazing, and surprisingly stable, and it wouldn't be this way without the commmunity that helped and contribute to the project! Some notable names:

@crystall1nedev - Project manager, iOS port developer  
@khanhduytran0 - iOS port developer  
@artdeell  
@Mathius-Boulay  
@zhuowei  
@jkcoxson   
@Diatrus 

## Third party components and their licenses
- [Caciocavallo](https://github.com/PojavLauncherTeam/caciocavallo): [GNU GPLv2 License](https://github.com/PojavLauncherTeam/caciocavallo/blob/master/LICENSE).
- [jsr305](https://code.google.com/p/jsr-305): [3-Clause BSD License](http://opensource.org/licenses/BSD-3-Clause).
- [Boardwalk](https://github.com/zhuowei/Boardwalk): [Apache 2.0 License](https://github.com/zhuowei/Boardwalk/blob/master/LICENSE) 
- [GL4ES](https://github.com/ptitSeb/gl4es) by @lunixbochs @ptitSeb: [MIT License](https://github.com/ptitSeb/gl4es/blob/master/LICENSE).
- [Mesa 3D Graphics Library](https://gitlab.freedesktop.org/mesa/mesa): [MIT License](https://docs.mesa3d.org/license.html).
- [MetalANGLE](https://github.com/khanhduytran0/metalangle) by @kakashidinho and ANGLE team: [BSD 2.0 License](https://github.com/kakashidinho/metalangle/blob/master/LICENSE).
- [MoltenVK](https://github.com/KhronosGroup/MoltenVK): [Apache 2.0 License](https://github.com/KhronosGroup/MoltenVK/blob/master/LICENSE).
- [openal-soft](https://github.com/kcat/openal-soft): [LGPLv2 License](https://github.com/kcat/openal-soft/blob/master/COPYING).
- [Azul Zulu JDK](https://www.azul.com/downloads/?package=jdk): [GNU GPLv2 License](https://openjdk.java.net/legal/gplv2+ce.html).
- [LWJGL3](https://github.com/PojavLauncherTeam/lwjgl3): [BSD-3 License](https://github.com/LWJGL/lwjgl3/blob/master/LICENSE.md).
- [LWJGLX](https://github.com/PojavLauncherTeam/lwjglx) (LWJGL2 API compatibility layer for LWJGL3): unknown license.
- [DBNumberedSlider](https://github.com/khanhduytran0/DBNumberedSlider): [Apache 2.0 License](https://github.com/immago/DBNumberedSlider/blob/master/LICENSE)
- [fishhook](https://github.com/khanhduytran0/fishhook): [BSD-3 License](https://github.com/facebook/fishhook/blob/main/LICENSE).
- [shaderc](https://github.com/khanhduytran0/shaderc) (used by Vulkan rendering mods): [Apache 2.0 License](https://github.com/google/shaderc/blob/main/LICENSE).
- [NRFileManager](https://github.com/mozilla-mobile/firefox-ios/tree/b2f89ac40835c5988a1a3eb642982544e00f0f90/ThirdParty/NRFileManager): [MPL-2.0 License](https://www.mozilla.org/en-US/MPL/2.0)
- [AltKit](https://github.com/rileytestut/AltKit)
- [UnzipKit](https://github.com/abbeycode/UnzipKit): [BSD-2 License](https://github.com/abbeycode/UnzipKit/blob/master/LICENSE).
- [DyldDeNeuralyzer](https://github.com/xpn/DyldDeNeuralyzer): bypasses Library Validation for loading external runtime
- Thanks to [MCHeads](https://mc-heads.net) for providing Minecraft avatars.
