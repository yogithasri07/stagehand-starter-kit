# Troubleshooting Guide

This guide covers common issues that may occur when working with a StageHand-style voice control system connected to TouchDesigner through MCP.

## 1. The Voice Client Does Not Start

**Possible causes**
- Python is not installed or is unavailable in the terminal.
- The virtual environment is not activated.
- Required Python packages are missing.
- The command is being run from the wrong directory.

**Things to check**
1. Open PowerShell in the project directory.
2. Activate the virtual environment if the project uses one.
3. Confirm that Python is available:

   ```powershell
   python --version
   ```

4. Check the terminal output for the specific error.

## 2. The Microphone Is Not Working

**Possible causes**
- The wrong microphone is selected.
- Microphone permission is disabled.
- Another application is using the microphone.
- The audio input library is not configured correctly.

**Things to check**
- Check Windows microphone permissions.
- Confirm the intended input device is available.
- Close applications that may be using the microphone.
- Review the voice client's error messages.

## 3. Speech Is Not Recognised

**Possible causes**
- Background noise or unclear speech.
- The spoken phrase is not supported by the command parser.
- The speech recognition service is unavailable.
- An internet connection is required but unavailable.

**Things to try**
- Speak clearly and use a short command.
- Test with a known supported phrase.
- Check the speech recognition error output.
- Verify network access if your speech recognition service requires it.

## 4. The MCP Server Is Not Responding

**Possible causes**
- The server is not running.
- The client is using the wrong endpoint.
- The configured port is already in use.
- A connection or configuration error occurred.

**Things to check**
- Confirm that the MCP server process is running.
- Verify the endpoint configured in the client.
- Review the server terminal for error messages.
- Check that the required local services are available.

Do not change server configuration without first checking the existing working setup.

## 5. TouchDesigner Does Not React to Commands

**Possible causes**
- TouchDesigner is not running.
- The relevant project or network is not loaded.
- A command failed before reaching TouchDesigner.
- The visual control mapping is not configured as expected.

**Things to try**
- Confirm TouchDesigner is open.
- Check the MCP server and client output.
- Test a simple supported command.
- Verify the connection between the server and the TouchDesigner project.

## 6. A Command Is Not Recognised

**Possible causes**
- The spoken phrase differs from the phrases supported by the command parser.
- The requested look or action is not available.
- Speech recognition returned unexpected text.

**Things to try**
- Use a documented example from `examples/voice_commands.md`.
- Check the recognised text in the client output.
- Confirm that the requested look or action is supported.

## 7. General Debugging Checklist

Before making code changes, check the following:

- [ ] Python and the required dependencies are available.
- [ ] The correct virtual environment is active.
- [ ] TouchDesigner is running.
- [ ] The MCP server is running.
- [ ] The voice client can access the microphone.
- [ ] The configured endpoint and port are correct.
- [ ] The command is supported by the current implementation.
- [ ] The terminal output has been checked for errors.

## Security Reminder

Never share passwords, access tokens, API keys, or other private credentials in public issues or repository files.

## Contributing Improvements

If you discover a new issue, consider documenting:
- What happened.
- What you expected to happen.
- The error message, with sensitive details removed.
- The steps that resolved the issue.

This guide is intended as a general troubleshooting resource. Individual fixes should be verified against the specific project configuration.
