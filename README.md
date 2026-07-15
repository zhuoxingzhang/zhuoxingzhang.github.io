# zhuoxingzhang.github.io

Personal academic site. Plain Jekyll — GitHub Pages builds it on every push, so
there is nothing to install and nothing to run.

## How to update

All content lives in `_data/`. You never need to touch HTML or CSS.

| I want to…                          | Edit                    |
| ----------------------------------- | ----------------------- |
| Add a paper                         | `_data/publications.yml` |
| Post a news item                    | `_data/news.yml`         |
| Change bio, interests, links, email | `_data/profile.yml`      |
| Change the site title / SEO blurb   | `_config.yml`            |

Edit the file, commit, push. The site rebuilds in about a minute.

You can do this entirely in the browser: open the file on GitHub, click the
pencil icon, edit, and hit *Commit changes*.

### Adding a paper

Copy an existing block in `_data/publications.yml` and change the fields. Only
`title`, `authors`, `venue`, `year`, and `type` are required.

```yaml
- title: The title of the paper
  authors: Yanni Tang, Zhuoxing Zhang, Sebastian Link
  venue: SIGMOD
  venue_full: Proceedings of the ACM on Management of Data   # tooltip on the venue tag
  year: 2027
  type: conference        # journal | conference
  award: Best Paper       # optional
  links:                  # optional
    - {name: DOI, url: "https://doi.org/10.1145/xxxxxxx"}
    - {name: PDF, url: "/assets/papers/my-paper.pdf"}
    - {name: Code, url: "https://github.com/zhuoxingzhang/..."}
```

Order in the file does not matter — the page groups by `year` and sorts newest
first. Your name is bolded automatically (it matches `author_name` in
`_config.yml`).

### Changing the photo

The current photo is `images/zhuoxing.jpg`. To swap it, drop a new square image
in `images/` and point `_data/profile.yml` at it:

```yaml
photo: "/images/my-new-photo.jpg"
```

Leave `photo: ""` and you get a typeset monogram instead.

### Adding a CV

Save it as `assets/cv.pdf`, then in `_data/profile.yml` set `cv: "/assets/cv.pdf"`.
A CV pill appears in the sidebar. Leave it empty to hide it.

## Deploying

Push to the `master` branch of `zhuoxingzhang/zhuoxingzhang.github.io`. In the
repo's *Settings → Pages*, source is **Deploy from a branch**, branch `master`,
folder `/ (root)`.

## Optional: previewing locally

Not required, but if you want to see changes before pushing and have Ruby
installed:

```bash
bundle install
bundle exec jekyll serve
```

Then open <http://localhost:4000>. Changes to `_data/` reload automatically;
changes to `_config.yml` need a restart.

## Structure

```
_config.yml            site settings, SEO
_data/profile.yml      name, bio, interests, links
_data/news.yml         news items (empty -> the News section hides itself)
_data/publications.yml papers
_layouts/default.html  page shell
_includes/sidebar.html sidebar
index.html             the page itself
assets/css/site.css    all styling (design tokens at the top)
images/                photos, incl. the profile picture
_portfolio/            dormant: 2025 South Island road-trip gallery, not linked
                       from the current site (see images/nz/)
```

Colours, fonts, and spacing are CSS variables in the `:root` block at the top of
`assets/css/site.css`. Dark mode follows the reader's system setting.

One gotcha worth knowing: because `_config.yml` names no theme, GitHub Pages
applies `jekyll-theme-primer` by default. That theme ships its own
`assets/css/style.scss`, which builds to `/assets/css/style.css` and would
silently override a file of ours at that path — which is why the stylesheet is
called `site.css`. Don't rename it back.
