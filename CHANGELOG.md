# Changelog

## [Unreleased]

## [0.1.3] - 2026-11-10

Needs Mouser 1.5 (frames, bubbles and the services below); Mouser 1.5 pins and installs it.

### Added

- A terminal-agent look: a rounded frame and message bubbles, fullscreen within its panel, slash commands (`/hf`, `/model`, `/new`, `/revoke`, `/help`).
- The agent can run commands on this computer (`terminal_run`) after Mouser's card with Allow / Allow all / Deny; Allow all lasts for the conversation and `/revoke` or `/new` ends it.
- Hugging Face: search GGUF models, read a model's details and install one (`h` or `/hf`); only architectures the bundled llama.cpp supports are offered, labelled "supported architecture, not load-tested".
- Pictures, video and sound named in messages or tool output play inline, each with fullscreen (mouser-media).
- Asks for `files.read` (to show media named in the chat).

### Changed

- Built on mouser-mode-api 0.3 and mouser-media 0.1.

## [0.1.2] - 2026-11-05

### Added

- Context menu (right-click, or `.` in Mouser 1.4): on a message copy, quote in a reply, retry, delete from view; on a tool card show / hide output, copy output, copy the call; elsewhere model, new chat, scroll (docs/chat.md §Context menu).
- The panel follows the size chosen in Mouser. Built on mouser-mode-api 0.2.

## [0.1.1] - 2026-11-05

### Fixed

- The Linux release is built on Ubuntu 22.04 (glibc 2.35), so it loads on older distributions too; 0.1.0 needed glibc 2.43.

## [0.1.0] - 2026-11-05

### Added

- First release on its own, extracted from [Mouser](https://github.com/WeirdBrains/mouser) with its history. Mouser's chat mode as a plugin: the agent runs in Mouser (models, keys, tools), this program draws the conversation.
