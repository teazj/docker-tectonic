# fabianhauser/tectonic

This docker image provides a preinstalled [tectonic](https://tectonic-typesetting.github.io/):

> Tectonic is a modernized, complete, self-contained TeX/LaTeX engine, powered by XeTeX and TeXLive.

## Usage (Linux)

```bash
# Create cache directory (manually, or docker creates it as root:root)
mkdir ~/.cache/docker-tectonic
docker run -ti --rm --volume ~/.cache/docker-tectonic:/home/tectonic/.cache:z --volume `pwd`:/tectonic:z fabianhauser/tectonic YourFile.tex
```

## Utilities

This image contains following utilities:

- `makeindex`
- `makeglossaries` from [glossaries](https://www.ctan.org/pkg/glossaries)

To use them, you have to change the `--entrypoint` to the according utility.
