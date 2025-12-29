📺 VlcMedia Plugin for Unreal Engine (WIP)








VlcMedia integrates libVLC streaming capabilities directly into Unreal Engine — allowing you to play .m3u8, livestream, and web video sources natively inside Blueprint-only projects without compiling C++.

Drop the included BP_TV actor into your level, assign a stream, press Play.
No source build required. No extra configuration. Just works.

✨ Features

🟢 .m3u8 livestream + URL media streaming

🟢 Ready-to-use BP_TV Blueprint actor

🟢 Precompiled plugin — no C++ required

🟢 Works in Editor + Packaged Builds

🟢 Auto MediaPlayer → MediaTexture → Material setup

🟢 Channel switching using MediaSource arrays

⚙️ Intended for Windows x64 (more platforms later)

🖥 Platform Support
Operating Systems
Platform	Status	Notes
Windows 10/11 (64-bit)	🟢 Supported	Fully tested in Editor & Packaged builds
macOS	🔴 Not Supported	No libVLC binaries currently included
Linux	🟡 Untested	May work with custom-built VLC libs
Android	🔴 Not Supported	Requires mobile libVLC pipeline
iOS	🔴 Not Supported	Not yet implemented
Unreal Engine Compatibility
UE Version	Status	Notes
5.4.4	🟢 Primary Build Target	Latest packaged release
5.2.1	⚠️ Legacy	Source-only; no ongoing support
Others	🔴 Unsupported	Untested + no provided builds
VLC / libVLC Requirements

A 64-bit installation of VLC is required.

This plugin dynamically loads:

libvlc.dll
libvlccore.dll


If VLC is not installed (or only 32-bit installed), playback cannot initialize.

📦 Installation

Download the latest packaged release.

Extract into your project's plugin directory:

YourProject/
 └── Plugins/
     └── VlcMedia/
         ├── Binaries/
         ├── Config/
         ├── Content/
         │   └── BP_TV.uasset
         ├── Resources/
         ├── VlcMedia.uplugin
         └── README.md


Open your Unreal Project → enable plugin if prompted.

Drag BP_TV into any level to begin streaming.

🟢 No compiling required — plug in & go.

🧠 Setup Guide

This plugin is based on the workflow from
📺 Timo Helmers — Streaming Blueprint Tutorial
https://www.youtube.com/watch?v=nNNzUf3zNjM&t=2s

Using BP_TV Actor

Place BP_TV into your scene

Open it and configure the ChannelList (StreamMediaSource Array)

Set ChannelIndex to auto-play a specific stream

Press Play — the video should start immediately

Blueprint logic example:

🧪 Example Streams

Use these streams for testing:

NASA TV — https://nasatv-lh.akamaihd.net/i/NASA_101@319270/master.m3u8

DW English — https://dwstream4-lh.akamaihd.net/i/dwstream4_live@123456/master.m3u8

⚠️ Some streams may block external playback or have geo restrictions.

📚 Documentation

📘 Wiki — https://github.com/Jon1969Edwards/VlcMedia_UnrealEngine/wiki/%F0%9F%8F%A0-Home

📄 VideoLAN Docs — https://www.videolan.org/doc/

🛠 Troubleshooting
Issue	Fix
Video doesn't play	Ensure VLC x64 is installed
Black screen	Verify Media Source URL works externally
Plugin loads but no video	Check firewall/stream authentication
Channel list empty	Add StreamMediaSource assets in Content
📜 License

This plugin is proprietary.
Redistribution, resale, re-upload, or public posting of binaries or source is not permitted outside of official distribution channels.

Forks are allowed for internal use & contribution only, and must retain:

Author credit (Jon Edwards / Virtual World Resources)

This license section

Copyright notice inside LICENSE.md

Commercial usage permitted for verified purchasers.
Full legal terms → LICENSE.md

🧾 Credits

Developed by Jon Edwards

Special thanks to Charles (age 9) for testing + feature ideas 🎮

Uses VLC backend via VideoLAN / libVLC

☕ Support Development

If this plugin helped you — you can support continued updates:

<a href='https://ko-fi.com/Z8Z81F4OEC' target='_blank'> <img height='36' src='https://storage.ko-fi.com/cdn/kofi6.png?v=6' alt='Buy Me a Beer on Ko-Fi'> </a>