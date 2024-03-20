

magicq-flatpak
===============

This repo allows you to package Chamsys MagicQ as a Flatpak for use on Linux Flatpak
based systems, especially e.g. Fedora Silverblue where there aren't easier installation
options. 

Usage
-----

1. Clone this repo with: `git clone https://github.com/RobotRoss/magicq-flatpak.git --recursive`
By default, com.blackmagic.Resolve.yaml is configured to package the latest version of Resolve (18.5 Beta 3 at the time of writing).

2. Build your package, and export to a distributable single file installer:

```
flatpak-builder --force-clean --repo=repo build-dir com.chamsyslighting.magicq.yaml
flatpak build-bundle repo magicq.flatpak com.chamsyslighting.magicq.yaml
```

3. Install the bundle using your package manager.

4. Enjoy.
