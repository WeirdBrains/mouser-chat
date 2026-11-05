# mouser-chat

Mouser's chat mode as a plugin: the agent runs in Mouser (models, keys, tools), this program draws the conversation.

Part of [Mouser](https://github.com/WeirdBrains/mouser), the terminal emulator. It is one of Mouser's official modes, built on the same public API anyone can use ([mouser-mode-api](https://github.com/WeirdBrains/mouser-mode-api)).

## Install

Mouser installs it on first start. To install or update it yourself:

```sh
mouser plugin install chat            # the version this Mouser pins
mouser plugin install gh:WeirdBrains/mouser-chat   # the latest release
```

Or in Mouser: `esc :pi chat`.

## Build

```sh
cargo build --release
# then: mouser plugin install .   (plugin.toml runs ./mouser-chat)
```

## Documentation

- [docs/](docs/README.md)
- Mouser: [plugins](https://github.com/WeirdBrains/mouser/blob/main/docs/plugins.md), [engines](https://github.com/WeirdBrains/mouser/blob/main/docs/engines.md), [installing and updating](https://github.com/WeirdBrains/mouser/blob/main/docs/downloads.md)

## Releases and signatures

Published on [crates.io](https://crates.io/crates/mouser-chat). GitHub releases are signed with the WeirdBrains minisign key ([minisign.pub](minisign.pub), `61BA1720747F9146`), the key Mouser pins for official plugins and engines:

```sh
minisign -Vm FILE -P RWRGkX90IBe6YaOypKF9r1wz4OqpCp3Ggb1Ag2omAzxTRaqoHzsNQSdP
```

## License

BSD-3-Clause, see [LICENSE](LICENSE).
