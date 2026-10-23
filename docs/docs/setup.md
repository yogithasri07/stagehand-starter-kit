# Setup Guide

This guide explains the basic setup for a local StageHand-style voice control workflow with TouchDesigner and MCP.

## 1. Prerequisites

Before starting, you should have:

- Windows 10 or 11
- Python installed
- TouchDesigner installed
- A microphone for voice input
- Git (optional, for downloading repositories)
- A working StageHand MCP server and voice client

Some features may require an internet connection, depending on the speech recognition service being used.

## 2. Understand the Components

A typical workflow contains three main components:

1. **Voice client:** captures spoken commands and converts speech into text.
2. **MCP server:** exposes tools that the client can call.
3. **TouchDesigner:** receives the corresponding controls and updates the visual output.

The exact implementation depends on the project configuration.

## 3. Start the Services

For an existing local StageHand setup, open separate PowerShell windows for the required services.

Start the MCP server in its project directory:

```powershell
python stagehand_server.py
```

Start the voice client in another window:

```powershell
python voice_client.py
```

If the project uses a Python virtual environment, activate it first. For example:

```powershell
.\.venv\Scripts\Activate.ps1
```

Run these commands from the directory containing the relevant files.

## 4. Test a Command

Once the required services are running, try a simple command supported by your implementation, such as:

- Check status
- Change the look
- Adjust intensity

The available commands depend on the configured voice client and MCP tools.

## 5. Troubleshooting

If a command does not work:

- Confirm that TouchDesigner is running.
- Confirm that the MCP server is running.
- Confirm that the voice client can access your microphone.
- Check the terminal output for errors.
- Verify that the required dependencies are installed.

## 6. Security Notes

- Never publish passwords, tokens, API keys, or private configuration files.
- Review repository contents before committing.
- Check software licences before redistributing code.
- Do not assume that all speech recognition or cloud services are free.

## Status

This guide provides a general starting point. Verify each step against your actual StageHand implementation before relying on it as a tested installation procedure.
