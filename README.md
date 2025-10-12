# Dmytro Vorobiov — Personal Music Website

A minimalist, dark-themed, single-page site built with Jekyll and GitHub Pages.  
Focus: music releases with streaming links, a personal hero section, and simple contact.

## Structure

    .
    ├── _config.yml
    ├── _includes/
    │   ├── streaming-badges.html   # hero streaming links (Spotify/Apple/Bandcamp)
    │   └── release-badges.html     # per-release icons on Music section
    ├── _layouts/
    │   └── default.html            # header, nav, footer, wrapper
    ├── _music/                     # one .md per release
    ├── assets/
    │   ├── css/style.css           # dark theme, layout
    │   ├── icons/                  # local SVGs: spotify.svg, apple.svg, bandcamp.svg, tiktok.svg, instagram.svg
    │   └── images/portrait.jpg     # hero portrait (replace with your photo)
    ├── index.md                    # single page: Hero (with bio), Music, Contact
    └── links.md                    # link-in-bio page for TikTok/Instagram

## Hero (portrait + bio)
- Side-by-side layout on desktop, stacked on mobile.
- Portrait file: `assets/images/portrait.jpg`.
- Streaming badges rendered via `_includes/streaming-badges.html`.

## Music
- Renders cards from `_music/` collection.
- Example front matter for a release:

        ---
        title: "Wandering Spaces"
        cover: "/assets/images/wandering-spaces.jpg"
        release_date: "2025-09-01"
        description: "First single from the upcoming album."
        platforms:
          - name: spotify
            url: https://open.spotify.com/track/XXXX
          - name: apple
            url: https://music.apple.com/album/XXXX
          - name: bandcamp
            url: https://yourname.bandcamp.com/track/XXXX
        ---

- Platform icons are **local SVGs** in `assets/icons/`.

## Contact
- TikTok and Instagram icons **with text labels** in the Contact section.
- Configure links in `_config.yml`:

        social:
          - name: tiktok
            url: https://www.tiktok.com/@yourhandle
          - name: instagram
            url: https://www.instagram.com/yourhandle

## Theme / Colors
- Accent color (matches album art): set in `assets/css/style.css`

        :root { --accent: #d46426; }

- Links and subtle accents use `var(--accent)`.

## Local Preview & Deploy
- Local:

        bundle install
        bundle exec jekyll serve
        # open http://localhost:4000

- Deploy: push to GitHub; Pages builds automatically.

## Maintenance
- Add/edit releases in `_music/`.
- Replace portrait at `assets/images/portrait.jpg`.
- Update socials in `_config.yml`.
- Streaming badges/icons live in `_includes/…` and `assets/icons/`.

## Optional Next Steps
- OG/Twitter preview image + metadata.
- Lightweight analytics (Plausible/Fathom).
- Mailing list integration (later).

