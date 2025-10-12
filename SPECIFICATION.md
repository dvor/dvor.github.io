
---

### `SPECIFICATION.md`
```markdown
# Website Specification — Dmytro Vorobiov

## 1) Purpose
Public hub for Dmytro Vorobiov as a **musician**. Prioritizes listening (Spotify/Apple/Bandcamp), quick personal context, and easy contact. No tech résumé focus.

## 2) Audience
- Listeners from TikTok/Instagram and streaming platforms
- Fans exploring more music
- Potential collaborators / media

## 3) Information Architecture (Single Page + Links)
- **Hero** (portrait, name, short bio, streaming badges)
- **Music** (release cards from `_music/`)
- **Contact** (TikTok, Instagram with icons + labels)
- **Links page** (`/links`) for TikTok/Instagram bio (streaming badges + socials)

## 4) Visual / UX
- Dark, minimalist layout; mobile-first.
- **Hero side-by-side**: photo left, text + badges right; stacks on mobile.
- Accent color **#d46426** (rust orange from album art).
- Local SVG icons for Spotify, Apple Music, Bandcamp, TikTok, Instagram.
- Smooth anchor scrolling; simple top nav: `Home | Music | Contact`.

## 5) Content Model
- `_music/*.md` with front matter:
  - `title` (string)
  - `cover` (path, optional)
  - `release_date` (YYYY-MM-DD)
  - `description` (short text)
  - `platforms` (array of `{name: spotify|apple|bandcamp, url: ...}`)
- `assets/images/portrait.jpg` for hero image.
- Social links editable in `_config.yml`.

## 6) Technical Stack
- **Jekyll** on **GitHub Pages**.
- HTML + Liquid + CSS; no JS required for core features.
- Includes:
  - `_includes/streaming-badges.html`
  - `_includes/release-badges.html`
- Local SVG icons in `assets/icons/`.

## 7) Accessibility & Performance
- High contrast on dark background.
- Alt text on images (portrait, covers).
- Responsive images; lightweight SVG icons (local).
- Minimal dependencies; fast page load.

## 8) Non-Goals (Launch)
- No blog or news feed.
- No live shows/ticketing.
- No mailing list (reserved for future).
- No analytics initially.

## 9) Future Enhancements
- OG/Twitter metadata and default share image.
- Optional analytics (Plausible/Fathom).
- Mailing list integration.
- Press kit (EPK) page if outreach begins.

