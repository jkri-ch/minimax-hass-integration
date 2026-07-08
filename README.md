<!-- markdownlint-disable first-line-heading -->
<!-- markdownlint-disable no-inline-html -->

<img src="https://play-lh.googleusercontent.com/hsPVehKUDPBS1LiaAkitNSmZtVNjb5-zbnlhHuNid42l5RMWWVEEiHqF5vSawdNK6ro"
     alt="MiniMax icon"
     width="35%"
     align="right"
     style="float: right; margin: 10px 0px 20px 20px;" />

[![GitHub Release](https://img.shields.io/github/release/jkri-ch/minimax-hass-integration.svg?style=flat-square)](https://github.com/jkri-ch/minimax-hass-integration/releases)
[![Build Status](https://img.shields.io/github/actions/workflow/status/jkri-ch/minimax-hass-integration/tests.yaml?branch=master&style=flat-square)](https://github.com/jkri-ch/minimax-hass-integration/actions/workflows/tests.yaml)
[![Test Coverage](https://img.shields.io/codecov/c/gh/jkri-ch/minimax-hass-integration?style=flat-square)](https://app.codecov.io/gh/jkri-ch/minimax-hass-integration/)
[![License](https://img.shields.io/github/license/jkri-ch/minimax-hass-integration.svg?style=flat-square)](LICENSE)
[![hacs](https://img.shields.io/badge/HACS-default-orange.svg?style=flat-square)](https://hacs.xyz)

# MiniMax Home Assistant Integration

Provides conversation, text-to-speech (TTS), and speech-to-text (STT) capabilities powered by MiniMax AI.

## Features

- **Conversation Agent**: Natural language conversations powered by MiniMax-M3
  (1M context) or the M2.x family
- **Text-to-Speech**: High-quality voice synthesis with selectable speech model
  (Speech 2.8 HD/Turbo and earlier) and customizable voices
- **Speech-to-Text**: Audio transcription for voice commands

> [!NOTE]
> MiniMax does not currently offer a public speech-to-text API, so the STT
> entity will return an error until MiniMax ships one. For a working voice
> pipeline today, pair the MiniMax conversation agent and TTS with a local STT
> engine such as the Whisper add-on.

## Installation

Easiest install is via [HACS](https://hacs.xyz/):

[![Open your Home Assistant instance and open a repository inside the Home Assistant Community Store.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=jkri-ch&repository=minimax-hass-integration&category=integration)

`HACS -> Integrations -> Explore & Add Repositories -> MiniMax`

For manual installation for advanced users, copy `custom_components/minimax` to
your `custom_components` folder in Home Assistant.

## Configuration

After installation:

1. Go to **Configuration > Integrations**
2. Click **Add Integration**
3. Search for **MiniMax**
4. Enter your MiniMax API key

### Subentries

The integration creates three subentries for independent configuration:

- **Conversation**: Configure the AI model and system prompt
- **TTS**: Select voice, speed, pitch, and volume
- **STT**: Configure transcription prompt

## Requirements

- Home Assistant 2025.4.1 or later
- MiniMax API key from [MiniMax Platform](https://platform.minimax.io)

## License

MIT License
