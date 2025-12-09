📌 KeylanceSDK — Remote Protection & Licensing for Unreal Engine (5.3 → 5.7)

KeylanceSDK is a lightweight security system designed to lock any Unreal Engine executable (.exe) through a remote license check.
It lets you activate or disable a build at any time, manage expiration dates, and keep full control over client deliveries.

➡️ Compatible with UE 5.3 → 5.7
➡️ C++ subsystem
➡️ Online API + offline fallback
➡️ Simple integration, fast deployment

Official website: https://aukkeproduction.fr/keylancehub

Documentation: https://aukkeproduction.fr/documentation

✨ Features

🔐 Remote key verification

📴 Works offline using cached protected data

📅 Cloud-based expiration date sync

🔄 Real-time activation/deactivation from your dashboard

🧩 Blueprint events for success/failure handling

🚫 Blocks execution when expired or revoked

⚙️ Extremely easy to integrate

📦 Installation

Download the latest release:
👉 https://github.com/Aukkeprod/KeylanceSDK/releases

Extract the ZIP

Copy KeylanceSDK into:

<YourProject>/Plugins/


Restart Unreal Engine

Enable the plugin in Edit → Plugins

🔑 Setup
1. Get your API credentials

Login to KeylanceHub → Create a project → Copy:

API Key

Project Key

2. Unreal Project Settings

Go to Project Settings → Keylance Protection and fill:

Apikey

ProjectKey

Enable bIsProtected

Done.

▶️ Usage
Check the license on startup (C++)
UKeylanceSubsystem* KL = GetGameInstance()->GetSubsystem<UKeylanceSubsystem>();
KL->CheckKey();

Events Blueprint

OnRequestSuccess → license valid

OnRequestFailed → invalid/expired

OnProjectUnprotected → server protection disabled

🛡️ Offline behavior

If the server is unreachable, KeylanceSDK safely falls back on:

locally cached expiration date

previous server validation

local protection flag

If the stored expiration date is passed → the project remains locked.

📁 Plugin structure

KeylanceSubsystem → main logic

LocalDataSave → encrypted offline store

ExposeOnPS → project settings

Server-side: VerifKey.php for API validation

🧩 Minimal Blueprint setup

Open your GameInstance

Use Event Init

Call Get Keylance Subsystem → Check Key

Bind events:

success → start your game

fail → quit or display a message

📄 License

Developed by Aukke Production
© 2025 — All rights reserved.
