# PP Projekt public site

Site deployed at http://pproj.net using Cloudflare sites.

This is the public facing home site for the PProj event.
It is not intended to give out any detail about the event.

This is intended to give an idea for outsiders/newcomers on what this event is about, when we are doing PR work.

## magic command for image scaling

**Please, do this before committing any new image to the repository!**

```bash
convert infile.jpg -auto-orient -resize '1920x' -quality 90 -strip outfile.jpg
```

**Note:** adjust the size and quality to your liking. `-strip` removes all metadata.

Do it in batch:

```bash
i=0; for f in *; do convert $f -auto-orient -resize '1920x' -quality 90 -strip $i.jpg; i=$(( $i + 1 )); done
```

**Note:** `-auto-orient` actually prevents imagemagick from rotating the image around.

## Template

This site is based on the [Hugo Scroll](https://themes.gohugo.io/themes/hugo-scroll/) template.

## Sponsor logos

Sponsor logos are fake companies of our friends for now. May change in the future.

## About the secrets

Yes, you are in the right place, keep going. You might want to check out the code snippet that instructed you to go on secret hunt in the first place.
