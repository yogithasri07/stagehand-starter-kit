# StageHand Starter Kit

**A beginner-friendly guide to voice-controlled visual workflows using TouchDesigner and the Model Context Protocol (MCP).**

StageHand explores how spoken commands can be translated into tool calls that control visual experiences in TouchDesigner. This starter kit provides documentation, examples, and troubleshooting guidance to help beginners understand the workflow.

## Why This Project?

Connecting voice input, tool interfaces, and visual software can be challenging for beginners. This project aims to make that process easier to understand through clear explanations and practical examples.

## How It Works

The workflow has three main components:

1. **Voice Client** — captures speech and converts it into text.
2. **MCP Server** — exposes tools that the client can invoke.
3. **TouchDesigner** — responds to supported controls and updates the visual output.

### Architecture

```text
       Spoken Command
              |
              v
      +----------------+
      |  Voice Client  |
      | Speech to Text |
      +----------------+
              |
              v
      +----------------+
      |   MCP Server   |
      | Available Tools|
      +----------------+
              |
              v
      +----------------+
      | TouchDesigner  |
      | Visual Output  |
      +----------------+
```

## Example Use Cases

Depending on the connected implementation, voice commands may be used to:

- Check the current visual status.
- Switch between visual presets.
- Adjust visual intensity.
- Control glow settings.
- Trigger predefined visual moments.
- Restore a previous visual configuration.

See [`examples/voice_commands.md`](examples/voice_commands.md) for command examples.


## Getting Started

1. Review the prerequisites in [`docs/setup.md`](setup.md).
2. Follow the setup instructions for your own environment.
3. Start the required local services.
4. Try a supported voice command.
5. Consult [`docs/troubleshooting.md`](docs/troubleshooting.md) if something does not work.

This repository is a companion learning resource. Refer to the primary [StageHand project](https://github.com/yogithasri07/stagehand) for the main implementation.

## Who Is This For?

- Beginners exploring TouchDesigner.
- Developers learning about MCP integrations.
- Creators interested in voice-controlled visual experiences.
- Contributors who want to improve beginner-friendly technical documentation.

## Contributing

Documentation improvements, new examples, and troubleshooting tips are welcome.

Please read [`CONTRIBUTING.md`](CONTRIBUTING.md) before contributing.

## Security and Privacy

- Never commit passwords, access tokens, or API keys.
- Review files before publishing them.
- Check the licensing requirements of external dependencies.
- Verify commands before using them in a live visual environment.

## Licence

This project uses the MIT License. See [`LICENSE`](LICENSE) for details.
