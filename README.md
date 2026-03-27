# Mkraftman Sony Blu-ray Media Control

A custom Home Assistant Lovelace card for controlling Sony Blu-ray players (e.g., UBP-X1100ES) via `rest_command`.

## Features

- Transport controls: Previous, Rewind, Play/Pause, Fast Forward, Next
- Long-press Play/Pause button to send Stop command
- Permanent Sony Blu-ray artwork background
- Responsive layout with ResizeObserver

## Installation

### HACS (Recommended)

1. Open HACS in Home Assistant
2. Go to **Frontend** > **Custom repositories**
3. Add `https://github.com/mkraftman/mkraftman-sony-bluray-media-control` as a **Lovelace** repository
4. Install **Mkraftman Sony Blu-ray Media Control**
5. Restart Home Assistant

### Manual

1. Download `mkraftman-sony-bluray-media-control.js` from the [latest release](https://github.com/mkraftman/mkraftman-sony-bluray-media-control/releases/latest)
2. Copy it to `/config/www/community/mkraftman-sony-bluray-media-control/`
3. Add the resource in **Settings > Dashboards > Resources**:
   - URL: `/local/community/mkraftman-sony-bluray-media-control/mkraftman-sony-bluray-media-control.js`
   - Type: JavaScript Module

## Prerequisites

You must have `rest_command` services configured for your Sony Blu-ray player:

- `rest_command.sony_bluray_prev`
- `rest_command.sony_bluray_rewind`
- `rest_command.sony_bluray_pause` (play/pause toggle)
- `rest_command.sony_bluray_stop`
- `rest_command.sony_bluray_forward`
- `rest_command.sony_bluray_next`

## Usage

Add the card to your dashboard:

```yaml
type: custom:mkraftman-sony-bluray-media-control
```
