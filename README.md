<div align="center">

<img src="snap/gui/vleer.png" alt="Vleer logo" width="128" />

# Vleer

**Your local music, with lyrics, artwork and an equalizer.**

[![vleer](https://snapcraft.io/vleer/badge.svg)](https://snapcraft.io/vleer)
[![Base: core26](https://img.shields.io/badge/Base-core26-2C8C3C?logo=canonical&logoColor=white)](https://snapcraft.io/core26)
![Confinement: strict](https://img.shields.io/badge/Confinement-strict-2C8C3C)
[![Maintainer: sidaliteir](https://img.shields.io/badge/Maintainer-sidaliteir-2C8C3C?logo=snapcraft&logoColor=white)](https://snapcraft.io/publisher/sidaliteir)
![Architectures: amd64 and arm64](https://img.shields.io/badge/Architectures-amd64%20%7C%20arm64-2C8C3C?logo=linux&logoColor=white)

[Getting Started](#getting-started) · [Configure](#configure) · [Limitations](#limitations) · [Build](#build) · [Support](#support) · [License](#license)

Unofficial snap packaging for [Vleer](https://github.com/vleerapp/vleer), a native local music player. This is a development snapshot.

</div>

---

## Getting Started

<a href="https://snapcraft.io/vleer"><img alt="Get it from the Snap Store" src="https://snapcraft.io/en/dark/install.svg" width="180"></a>

```bash
sudo snap install vleer --edge
vleer
```

Add a music folder from your home directory in the app.

## Configure

Manage music folders, playback and appearance in the app. There are no `snap set` options.

| Optional access | Command |
| --- | --- |
| Music on removable storage | `sudo snap connect vleer:removable-media` |

Library data and caches stay in `~/snap/vleer/common/` between updates.

## Limitations

- Upstream has no releases yet; only the edge channel is published. Roadmap streaming services are not implemented yet.
- Last.fm requires upstream's private build credentials and is unavailable in this build. Discord Rich Presence cannot reach a host Discord installation.
- Settings from a native installation are not imported automatically. Updates are managed by snapd.

## Build

Automated builds are deferred until the shared workflow supports commit-only upstreams.

```bash
git clone https://github.com/sidalit/vleer-snap.git
cd vleer-snap
sudo snap install snapcraft --classic
snapcraft pack
```

## Support

- **Installation or snap issues:** [open a packaging issue](https://github.com/sidalit/vleer-snap/issues).
- **Application bugs:** [report them upstream](https://github.com/vleerapp/vleer/issues).

## License

Snap packaging: [MIT](https://github.com/sidalit/vleer-snap/blob/main/LICENSE).
