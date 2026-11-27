# verazhengdesign.github.io

Personal portfolio site for **Vera Zheng — Product Designer & Research Analyst**.

Live: <https://verazhengdesign.github.io/>

## Bilingual structure

- English pages live at the repository root.
- Chinese pages live under `/zh/`.
- Page shells, navigation, footer, and language switch are shared through Jekyll.

| File | Purpose |
|---|---|
| `_config.yml` | Jekyll configuration |
| `_layouts/default.html` | Shared HTML shell + SEO/language metadata |
| `_includes/header.html` | Shared navigation + language switch |
| `_includes/footer.html` | Shared footer |
| `index.html` / `zh/index.html` | Homepage |
| `about.html` / `zh/about.html` | About page |
| `journal.html` / `zh/journal.html` | Journal index |
| `work/*.html` | Case studies (English; Chinese versions coming) |
| `styles.css` | Shared styles for every page and both languages |
| `assets/` | Images, project covers, tool icons |

Pages use front matter like:

```yaml
---
layout: default
lang: zh
ref: home
title: 页面标题
description: 页面描述
permalink: /zh/
---
```

The language switch matches pages by `ref`. When adding a translated page, give it the same `ref` as the English page and set `lang` accordingly.

## Editing

Edit the source files and push to `main`. GitHub Pages builds Jekyll automatically and redeploys in about a minute.

For local preview, build the site with Jekyll and serve the generated `_site` folder:

```bash
jekyll build
python3 -m http.server 4173 --directory _site
```

Do not serve the repository root directly: `index.html` and `about.html` use Jekyll layouts.
