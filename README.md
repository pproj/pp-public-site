# PP Projekt public site

Site deployed at http://pproj.net using Cloudflare sites.

This is the public facing home site for the PProj event.
It is not intended to give out any detail about the event.

This is intended to give an idea for outsiders/newcomers on what this event is about, when we are doing PR work.

## Image handling

### Scaling

**Please, do this before committing any new image to the repository!**

```bash
convert infile.jpg -auto-orient -resize '1920x' -quality 90 -strip outfile.jpg
```

**Note:** adjust the size and quality to your liking. `-strip` removes all metadata.

Do it in batch:

```bash
i=0; for f in *; do convert $f -auto-orient -resize '1920x' -quality 90 -strip $i.jpg; i=$(( $i + 1 )); done
```

**Note:** `-auto-orient` actually prevents imagemagick from rotating the image around. But it's pretty random.

### Shuffle

Shuffle the header images every so often.

see `layouts/partials/custom_header_video.html`

## Template

This site is based on the [Hugo Scroll](https://themes.gohugo.io/themes/hugo-scroll/) template.
