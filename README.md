# Home Assistant Blueprints

Reusable Home Assistant blueprints for UniFi Protect doorbells, Sonos, and Google TTS.

## Included blueprints

### UniFi Doorbell -> Sonos Google Announcement (Sync)

Best option for multi-room sync. Sends one announcement call to all selected Sonos players with one shared volume.

File:
- `automation/sonos-doorbell/unifi_doorbell_sonos_google_announce_sync.yaml`

[![Open your Home Assistant instance and import this blueprint.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/achecchia/home-assistant-blueprints/main/automation/sonos-doorbell/unifi_doorbell_sonos_google_announce_sync.yaml)

Raw import URL:

```text
https://raw.githubusercontent.com/achecchia/home-assistant-blueprints/main/automation/sonos-doorbell/unifi_doorbell_sonos_google_announce_sync.yaml
```

### UniFi Doorbell -> Sonos Google Announcement (Per Speaker Volume)

Lets you assign a different announcement volume to each Sonos player. This can be slightly less synchronized because Home Assistant sends the announcement one speaker at a time.

File:
- `automation/sonos-doorbell/unifi_doorbell_sonos_google_announce_per_speaker.yaml`

[![Open your Home Assistant instance and import this blueprint.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/achecchia/home-assistant-blueprints/main/automation/sonos-doorbell/unifi_doorbell_sonos_google_announce_per_speaker.yaml)

Raw import URL:

```text
https://raw.githubusercontent.com/achecchia/home-assistant-blueprints/main/automation/sonos-doorbell/unifi_doorbell_sonos_google_announce_per_speaker.yaml
```

### Shelly 1 Gen4 -> Sonos Google Announcement (Sync)

Detects a single doorbell-button press using the Shelly input event entity, with configurable Google TTS announcement and cooldown. Configure the Shelly input as **Button** and output as **Detached**.

[![Import into Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/achecchia/home-assistant-blueprints/main/automation/sonos-doorbell/shelly_gen4_doorbell_sonos_google_announce_sync.yaml)

Raw import URL:

```text
https://raw.githubusercontent.com/achecchia/home-assistant-blueprints/main/automation/sonos-doorbell/shelly_gen4_doorbell_sonos_google_announce_sync.yaml
```

### Shelly 1 Gen4 -> Sonos Google Announcement (Per Speaker Volume)

Detects a single doorbell-button press using the Shelly input event entity, with configurable Google TTS announcement and cooldown. Configure the Shelly input as **Button** and output as **Detached**.

[![Import into Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/achecchia/home-assistant-blueprints/main/automation/sonos-doorbell/shelly_gen4_doorbell_sonos_google_announce_per_speaker.yaml)

Raw import URL:

```text
https://raw.githubusercontent.com/achecchia/home-assistant-blueprints/main/automation/sonos-doorbell/shelly_gen4_doorbell_sonos_google_announce_per_speaker.yaml
```

## Features

- Real UniFi Protect doorbell ring detection
- Sonos `announce: true` playback
- Google TTS media source support
- Shared-volume sync blueprint
- Per-speaker volume blueprint
- Duplicate or replay suppression with cooldown

## Requirements

- Home Assistant
- UniFi Protect integration (UniFi blueprints only)
- Shelly integration with a Shelly 1 Gen4 configured for Button / Detached (Shelly blueprints only)
- Sonos integration
- Google Translate TTS configured in Home Assistant

## Import into Home Assistant

In Home Assistant:

1. Go to **Settings -> Automations & scenes -> Blueprints**
2. Click **Import Blueprint**
3. Paste one of the raw GitHub URLs above

## Repo structure

```text
home-assistant-blueprints/
├── .gitignore
├── LICENSE
├── README.md
└── automation/
    └── sonos-doorbell/
        ├── unifi_doorbell_sonos_google_announce_sync.yaml
        ├── unifi_doorbell_sonos_google_announce_per_speaker.yaml
        ├── shelly_gen4_doorbell_sonos_google_announce_sync.yaml
        └── shelly_gen4_doorbell_sonos_google_announce_per_speaker.yaml
```

## Recommended usage

- Use the **Sync** blueprint by default
- Use the **Per Speaker Volume** blueprint only when a site needs different room volumes
- After creating an automation from a blueprint, use Home Assistant's automation editor to test actions

## License

This repository uses the MIT License.
