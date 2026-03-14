# Codex Mule

Dedicated Home Assistant repository for the `Codex Mule` add-on and optional Assist integration.

## Contents
- `repository.yaml`: Home Assistant add-on repository metadata
- `codex_mule/`: Home Assistant add-on
- `custom_components/codex_mule_conversation/`: Optional custom integration for Assist

## Install In Home Assistant

### Add-on repository
1. In Home Assistant, open `Settings -> Add-ons -> Add-on Store`.
2. Open the three-dot menu, then choose `Repositories`.
3. Add this repository URL:

```text
https://github.com/olekspa/codex_mule
```

4. Refresh the Add-on Store, then open `Codex Mule`.
5. Click `Install`.

### Add-on configuration
Set at least these options before starting the add-on:

- `relay_url`: URL of your Codex relay, for example `http://192.168.1.50:8765`
- `relay_token`: bearer token expected by the relay

Then click `Start` and open the add-on panel from the sidebar or add-on page.

## Optional Assist Integration
This repo also includes `custom_components/codex_mule_conversation/` if you want Home Assistant Assist to route requests through Codex Mule.

Manual install:
1. Copy `custom_components/codex_mule_conversation` into your Home Assistant `config/custom_components/` directory.
2. Restart Home Assistant.
3. Open `Settings -> Devices & Services -> Add Integration`.
4. Search for `Codex Mule Conversation Agent`.

## Notes
- The add-on uses Home Assistant ingress, so you do not need to expose a separate UI port.
- The relay itself must already be running somewhere your Home Assistant instance can reach.
- Current repository URL and metadata are set for `https://github.com/olekspa/codex_mule`.
