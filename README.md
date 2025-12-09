KeylanceSDK — Remote Protection for Unreal Engine (5.4 → 5.7)
Secure any packaged Unreal Engine build with remote license control.

KeylanceSDK is a plug-and-play system that lets you lock any Unreal Engine executable (.exe) using a remote license check.
You can activate, deactivate, or expire builds directly from your KeylanceHub dashboard.

✔ Compatible with UE 5.4 → 5.7
✔ Plug & Play
✔ Remote + offline validation
✔ Blueprint-ready
✔ Perfect for agencies, studios, freelancers, client deliveries

🔗 Official website: https://aukkeproduction.fr/keylancehub

📘 Documentation: https://aukkeproduction.fr/documentation

🔥 Features

🔐 Remote license verification

📴 Offline fallback (cached expiration)

📅 Automatic expiration sync

🔄 Enable/disable builds remotely

🧩 Includes a ready-to-use Blueprint actor

🚫 Blocks execution when invalid or expired

⚙️ Works in packaged .exe builds

📦 Download

👉 Latest versions (UE 5.4 → 5.7):
https://github.com/Aukkeprod/KeylanceSDK/releases

🛠️ Developer Setup (Quick Guide)
Ultra simple — Plug & Play
⚠️ Required once: convert your project to C++

Unreal cannot load a C++ plugin in a pure Blueprint project.

Convert your project by creating an empty class:
Tools → New C++ Class → None → Create Class

Your project remains fully Blueprint afterward.

✔️ Installation

Download the ZIP for your Unreal Engine version

Extract it

Drop the folder KeylanceSDK/ into:

<YourProject>/Plugins/


Restart Unreal Engine

Enable the plugin in Edit → Plugins

⚡ Plug & Play Usage
✔️ 1. Place the provided Blueprint actor in your level

Location inside the plugin:

Content/Keylance/Blueprints/BP_ExempleKeylance


Drag BP_ExempleKeylance into your main map.

✔️ 2. Fill in the parameters (Details panel)

API Key

Project Key

bIsProtected

That’s it.
No C++ coding required.

🎁 What the Blueprint handles automatically

License verification on startup

Cached offline validation

Expiration enforcement

Remote disable detection

Automatic Success / Failed events

Automatic blocking if invalid

You only drag one actor and set your keys.

📄 License

Developed by Aukke Production
© 2025 — All rights reserved.
