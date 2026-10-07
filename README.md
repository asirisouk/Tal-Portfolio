# Tal's site

A single page site (index.html) that reads its content from the JSON files in /data at startup. This is what lets Pages CMS edit the site through simple forms instead of code.

## Files

- `index.html` the whole site: layout, styling, and the logic that builds each page.
- `data/site.json` name, tagline, bio, footer line, social links, shop section descriptions.
- `data/works.json` illustrations, photographs, collages, and tattoo pieces.
- `data/flash.json` available tattoo flash designs.
- `data/products.json` items for sale on the Creations page.
- `data/musings.json` writing/blog entries.
- `assets/images/` where uploaded photos land.
- `.pages.yml` tells Pages CMS what forms to show for each file above.

## Publishing on GitHub Pages

1. Push this whole folder to a GitHub repository (keep the folder structure, including `data/` and `.pages.yml`).
2. In the repo, go to Settings, then Pages. Under Build and deployment, set Source to Deploy from a branch, branch main, folder / (root). Save.
3. The site publishes at your GitHub Pages address, usually within a couple of minutes.

Note: because the site loads its content with `fetch`, it only works when served over a real web address (like the GitHub Pages link, or `python3 -m http.server` while testing). Double-clicking `index.html` on your computer will show a message instead of the site, since browsers block that kind of file loading for security reasons.

## Letting Tal add and edit work, privately

1. Add Tal as a collaborator on the GitHub repo (Settings, then Collaborators).
2. Tal signs in at app.pagescms.org with their GitHub account and adds the repository.
3. From there Tal sees Artwork, Tattoo flash, Creations, Musings, and Site settings, each as a simple form with photo upload. Saving commits the change, and the live site updates within a minute or two.

There is no link to this dashboard anywhere on the public site, so visitors never see it.
