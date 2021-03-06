[![CI](https://github.com/maximbaz/docker-joypixels-fonts-build/actions/workflows/ci.yml/badge.svg)](https://github.com/maximbaz/docker-joypixels-fonts-build/actions/workflows/ci.yml)

# Build JoyPixels font files

## Usage:

This will clone the `joypixels/emoji-assets` repository and use it to compile the fonts:

```
$ docker pull maximbaz/joypixels-fonts-build
$ docker run --rm -v $(pwd):/fonts maximbaz/joypixels-fonts-build
```

If you have `joypixels/emoji-assets` already available, use the following commands:

```
$ docker pull maximbaz/joypixels-fonts-build
$ docker run --rm -v $(pwd):/fonts -v /path/to/emoji-assets:/assets maximbaz/joypixels-fonts-build
```

The compiled fonts will be placed in the current directory on the host.

## Supported fonts

The image can currently build the following fonts:

- `joypixels-android.ttf` for Android and Linux.

---

- Based on [base/devel](https://hub.docker.com/r/base/devel/) image.
- Updated daily with [GitHub actions](https://github.com/maximbaz/docker-joypixels-fonts-build/actions).
- Sources are on [Github](https://github.com/maximbaz/docker-joypixels-fonts-build).
