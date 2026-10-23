# Voice Command Examples

This document introduces example voice commands for a StageHand-style visual control workflow.

The commands below are based on the available tool categories in the StageHand project. Exact spoken phrases depend on the configured voice client.

## 1. Check Status

**Example phrases**
- "Check status"
- "What's the current status?"

**Purpose:** Ask the system for information about the current visual configuration.

## 2. Change the Visual Look

**Example phrases**
- "Set the look to neon"
- "Change the look to warm"
- "Switch to mono"

**Purpose:** Change the visual preset.

**Example presets:** `neon`, `warm`, `cold`, `mono`, `dream`

## 3. Adjust Intensity

**Example phrase**
- "Set intensity to 0.8"

**Purpose:** Adjust the intensity value supported by the connected visual controls.

Use a value that falls within the range accepted by your implementation.

## 4. Control Glow

**Example phrases**
- "Turn glow on"
- "Turn glow off"

**Purpose:** Change the glow setting if the connected implementation supports these phrases.

## 5. Trigger a Visual Moment

**Example phrases**
- "Trigger drop"
- "Trigger calm"
- "Trigger flash"

**Purpose:** Trigger a predefined visual moment.

**Example moments:** `drop`, `calm`, `flash`

## 6. Restore a Previous Look

**Example phrase**
- "Restore the previous look"

**Purpose:** Request restoration of a previously saved visual configuration, if supported by the connected client.

## Important Notes

- These are example phrases, not a guarantee that every wording is recognised.
- Voice recognition may require an internet connection, depending on the configured speech recognition service.
- Check the voice client and MCP server output if a command fails.
- Avoid testing commands in a live show until you have confirmed their behaviour.

## Contributing

If you add a new command, document its purpose, accepted phrases, expected behaviour, and any limitations.
