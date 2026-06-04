# Zeal Flatpak

[![Flathub Version](https://img.shields.io/flathub/v/org.zealdocs.Zeal?style=flat-square)](https://flathub.org/apps/org.zealdocs.Zeal)
[![Flathub Downloads](https://img.shields.io/flathub/downloads/org.zealdocs.Zeal?style=flat-square)](https://flathub.org/apps/org.zealdocs.Zeal)

Flatpak packaging for [Zeal](https://github.com/zealdocs/zeal), an offline documentation browser. Published on [Flathub](https://flathub.org/apps/org.zealdocs.Zeal).

## Installation

```shell
flatpak install flathub org.zealdocs.Zeal
```

## Building locally

```shell
flatpak install flathub org.flatpak.Builder
flatpak run org.flatpak.Builder --force-clean --sandbox --user --install-deps-from=flathub \
    --ccache --compose-url-policy=full --mirror-screenshots-url=https://dl.flathub.org/media \
    --repo=repo builddir org.zealdocs.Zeal.json
```

To lint the manifest and the resulting repository:

```shell
flatpak run --command=flatpak-builder-lint org.flatpak.Builder manifest org.zealdocs.Zeal.json
flatpak run --command=flatpak-builder-lint org.flatpak.Builder repo repo
```

## Reporting issues

* Application bugs: [zealdocs/zeal](https://github.com/zealdocs/zeal/issues).
* Packaging issues (installation, sandbox permissions, missing features specific to the Flatpak build): [this repository](https://github.com/flathub/org.zealdocs.Zeal/issues).
