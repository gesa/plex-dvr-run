# Plex DVR Postprocessor Easy Start

## Motivation

As of Plex Media Server v1.19.3, the postprocessing script _must_ be called from the Scripts directory inside the [application data directory](https://support.plex.tv/articles/202915258-where-is-the-plex-media-server-data-directory-located/). This allows you to quickly set up [plex-dvr](https://github.com/gesa/plex-dvr) on your server.

## Prerequisites

- **`comskip`:** https://github.com/erikkaashoek/Comskip
- **`comcut`:** https://github.com/BrettSheleski/comchap
- **`ccextractor`:** https://github.com/CCExtractor/ccextractor
- **`ffmpeg`:** https://ffmpeg.org/
- **`HandbrakeCLI`:** https://handbrake.fr/downloads.php

## Quick Start

```sh
# from (application data directory)/Scripts
git clone git@github.com:gesa/plex-dvr-run.git
cd plex-dvr-run
npm i
```

Then, in your Plex Media Server DVR settings, set your DVR's postprocessing script to `plex-dvr-run/run`.

## Configuration

To customize for your system after running the [quick start](#quick-start), run `npx plex-dvr --sample-config`. This will dump a sample config.json into the console, along with printing the config directory path.

### Comskip

Save your comskip.ini file in the config directory. See [the tuning document](http://www.kaashoek.com/files/tuning.htm) for more information.

### HandBrake

Run `HandBrakeCLI --help` to see a list of available enocoders on your system, replacing the value in the config with your choice. Run `HandBrakeCLI --encoder-preset-list [your encoder]` to see available presets, pick one to add to your config.

