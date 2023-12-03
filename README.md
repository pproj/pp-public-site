# PProj public site

Site deployed at http://pproj.net

## magic command for image scaling

```bash
convert infile.jpg -auto-orient -resize '1920x' -quality 90 -strip outfile.jpg
```

do it in a batch:

```bash
i=0; for f in *; do convert $f -auto-orient -resize '1920x' -quality 90 -strip $i.jpg; i=$(( $i + 1 )); done
```

**Note:** `-auto-orient` actually prevents imagemagick from rotating the image around
