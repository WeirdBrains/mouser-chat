# The chat mode

Mouser's chat mode as a plugin: the agent runs in Mouser (models, keys, tools), this program draws the conversation.

## Install

Mouser installs it on first start. To install or update it yourself:

```sh
mouser plugin install chat            # the version this Mouser pins
mouser plugin install gh:WeirdBrains/mouser-chat   # the latest release
```

Or in Mouser: `esc :pi chat`.

## Use

Open it from Mouser's mode line (`esc :` then its hotkey or name). Its keys are listed in
[plugin.toml](../plugin.toml) and shown by Mouser (`esc :help`). Permissions it asks for:
`agent.use`, and `files.read` to show pictures, video and sound named in the chat.
Version 0.1.5 needs Mouser 1.5 or later; on Mouser 1.6 and later Mouser draws and plays its pictures, video and sound.

## How it works

It is a separate program Mouser starts once and keeps running, speaking the
[mode protocol](https://github.com/WeirdBrains/mouser-mode-api/blob/main/docs/protocol.md)
over stdio, with images through shared memory. Mouser's own end-to-end tests drive it
through Mouser's adapter, so those tests live in [Mouser](https://github.com/WeirdBrains/mouser).
