Easily run [plex-dvr](https://github.com/gesa/plex-dvr-run) on your server.

```sh
# from the Scripts directory of your PMS data dir
g clone git@github.com:gesa/plex-dvr-run.git
cd plex-dvr-run
npm i
```

Then, in your Plex Media Server DVR settings, set your DVR's postprocessing script to `plex-dvr-run/run`.
