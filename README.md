NFC Light Toggle Blueprint for Home Assistant

A flexible Home Assistant blueprint that allows you to toggle lights using NFC tags, including support for brightness, color, smooth transitions, and logbook entries.

Perfect for multi-user households and for use with the Home Assistant Companion App on iOS and Android.

✨ Features

📱 NFC tag as trigger

🔁 Toggle functionality (On / Off)

💡 Configurable brightness (%)

🎨 Optional color

RGB or

Color temperature (Kelvin)

🌈 Smooth transition when turning lights on or off

📊 Logbook entries

Which user triggered the action

Which light was controlled

On / Off state

♻️ Reusable blueprint

🧩 No duplicated automations required

🔧 Requirements

Home Assistant 2022.8 or newer

Home Assistant Companion App

iOS or Android

NFC-capable smartphone

An NFC tag registered in Home Assistant

One or more light entities

📦 Installation
1️⃣ Import the Blueprint

Go to Settings → Automations & Scenes → Blueprints

Click Import Blueprint

Paste the YAML code from this repository

Save

⚙️ Usage

After importing the blueprint:

Create a new automation from the blueprint

Configure the following options:

NFC tag

Light entity

Brightness (%)

Transition duration (seconds)

Optional:

RGB color

or Color temperature (Kelvin)

➡️ The NFC tag will now reliably toggle the selected light.

🧠 Logic Overview
Light is OFF

Turn on with:

defined brightness

optional color

smooth transition

Logbook entry:

[User] turned [Light] ON (NFC)

Light is ON

Turn off with transition

Logbook entry:

[User] turned [Light] OFF (NFC)

📊 Logbook

All actions are recorded in the Home Assistant logbook:

User name (via trigger.context.user_id)

Light entity

Action (ON / OFF)

Trigger source: NFC

Ideal for:

Multi-user environments

Auditing & traceability

Debugging

🍎 iOS Notes

Due to iOS system restrictions:

📱 The iPhone must be unlocked
(Face ID / Touch ID is sufficient)

✅ No additional confirmation is required

ℹ️ iOS briefly shows a system banner (“NFC tag detected”)

🚫 NFC scans are not possible while the device is locked

➡️ These limitations are enforced by iOS and cannot be bypassed by Home Assistant.

🤖 Android Notes

NFC scans may work without unlocking (device-dependent)

In many cases, no confirmation dialog

Very fast trigger response

🛡️ Security

The blueprint supports:

User identification via trigger.context.user_id

Person mapping in Home Assistant

➡️ Automations can be extended to allow only specific users or devices.

🧩 Possible Extensions

The blueprint can easily be extended with:

🔒 User whitelist

🌗 Day/Night brightness or color

🛏️ Multiple lights per tag

📈 Per-user statistics or counters

🔔 Notifications

🤝 Contributing

Contributions, ideas, and pull requests are welcome.
Please describe changes clearly and concisely.

📄 License

MIT License
Free to use, modify, and distribute.
