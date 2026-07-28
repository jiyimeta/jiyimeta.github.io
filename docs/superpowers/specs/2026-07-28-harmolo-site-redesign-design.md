# Harmolo site redesign — design

Date: 2026-07-28

## Problem

The site renders as unstyled Markdown. Three concrete problems:

1. **No design.** `_config.yml` declares no theme and the repo has no layouts, so GitHub Pages
   falls back to its default theme on `.html` output. The result looks like a raw document.
2. **The locale pages rely on GitHub Pages' implicit plugins.** The pages carry no front matter
   and no layout; they render only because GitHub Pages force-enables `jekyll-optional-front-matter`,
   `jekyll-default-layout` and `jekyll-relative-links`. The switcher works today because that last
   plugin rewrites the `.md` links to `.html`, but nothing in the repo says so. Making the pages
   explicit removes that hidden dependency.
3. **Every locale duplicates the app list.** Icon, name, description and store links are repeated
   in all 13 locale files. Adding one app means editing 13 files (as just happened with Synced
   Metronome).

## Goals

A polished single-page site per locale, with the app data held in one place.

Non-goals: per-app detail pages, screenshots, marketing copy beyond the existing one-liners.

## Design

### Source structure

App data and translations move into `_data`; the locale pages become front-matter-only stubs.

```
_config.yml            # defaults, no theme
Gemfile                # github-pages gem, pinned to match production
_data/
  apps.yml             # 5 apps: id, icon, store links (language-independent)
  i18n.yml             # 13 locales x UI strings + app descriptions
  locales.yml          # locale list: code, native name, path (switcher order)
_layouts/
  home.html            # hero + app grid + footer
  page.html            # prose pages (privacy policy)
_includes/
  head.html            # meta, title, hreflang alternates
  header.html          # wordmark + language switcher
  app-card.html        # one app card
  footer.html          # contact, privacy link, copyright
assets/css/style.css   # CSS custom properties, no build step
index.md, ja.md, ...   # front matter only (13 stubs)
privacy-policy/*.md    # prose kept as-is, layout: page added
icons/                 # unchanged
```

Adding an app touches exactly two files: `_data/apps.yml` and `_data/i18n.yml`.

### Page composition

- **Header** — `Harmolo` wordmark on the left, language switcher on the right. The switcher is a
  `<details>` dropdown listing all 13 locales in their native names, with the current one marked.
  No JavaScript.
- **Hero** — site name and tagline only, with generous whitespace.
- **App grid** — CSS Grid, one column on mobile and two from 720px up. Each card carries a 64px
  icon, the app name, the one-line description, and the store links.

### Store badges

App Store and Google Play links use each vendor's official localized badge, vendored into
`assets/badges/` by `Scripts/fetch-store-badges.py` and recorded in `_data/badges.yml`.

Google publishes only a black badge, so the row reads as black in both colour schemes. The web
link — which has no official badge — is a button built to the same recipe rather than to the page
palette: 40px tall, black, `#a6a6a6` border, 6px corner radius. Those numbers come from measuring
the artwork, where Apple's corner radius is 6.80px at 40px tall and Google's 3.96px, both bordered
in `#a6a6a6`. A button following the site's own light/dark tokens would look foreign beside two
fixed-colour badges.
- **Footer** — contact email, privacy policy link, copyright.

### Visual direction

Cool / Apple-like. Light and dark palettes are defined as CSS custom properties and swapped by
`prefers-color-scheme`. There is no theme toggle — that would need JavaScript, and the automatic
switch covers the case.

| token     | light     | dark      |
| --------- | --------- | --------- |
| `bg`      | `#FFFFFF` | `#000000` |
| `surface` | `#F5F5F7` | `#1D1D1F` |
| `border`  | `#D2D2D7` | `#38383D` |
| `text`    | `#1D1D1F` | `#F5F5F7` |
| `muted`   | `#6E6E73` | `#98989D` |
| `accent`  | `#0071E3` | `#2997FF` |

### URLs

Locale pages get explicit permalinks — `/` for English, `/ja/`, `/ko/`, `/zh-Hans/` and so on.
Privacy pages become `/privacy-policy/<locale>/`. Front matter also makes Jekyll render the files
instead of copying them, which is what fixes the raw-Markdown problem.

`jekyll-redirect-from` keeps the previously rendered `.html` paths (`/ja.html`) alive. The raw
`.md` URLs cannot be preserved — a file cannot be both rendered and copied — so any external link
pointing at a `.md` path has to be updated. The App Store Connect privacy policy URL is the one
known consumer and must be checked.

### Incidental fixes

- `<html lang>` is set per locale (currently always `en-US`).
- `hreflang` alternate links connect the 13 locales.
- `<title>` and `description` become locale-specific (currently "jiyimeta's homepage" everywhere).

## Local preview

`Gemfile` pins the `github-pages` gem so the local build matches production. Run under rbenv Ruby
3.1.1, which the gem supports:

```
rbenv local 3.1.1
bundle install
bundle exec jekyll serve
```

`_site/`, `vendor/` and `.jekyll-cache/` are gitignored.

## Verification

- The build succeeds with no warnings.
- 26 pages are generated: 13 home + 13 privacy.
- Every language-switcher link resolves to a rendered page (no `.md`, no 404).
- Screenshots at desktop and mobile widths, in light and dark mode.

## Contact address

The home page used to list `jiyi.meta@gmail.com` while the privacy policy listed
`contact@harmolo.com`. Both now use `contact@harmolo.com`, set once as `email` in `_config.yml`.
