# Paper Reader

Paper Reader is a minimal Hugo theme for calm long-form reading.

It is intentionally small: plain Hugo templates, one CSS file, no JavaScript, no asset pipeline, no npm install step. The theme works well for personal blogs, notes, essays, and Chinese-language writing.

## Features

- Clean typography for long articles
- Light and dark mode via `prefers-color-scheme`
- Responsive layout
- Home page post list
- Section, taxonomy, and term list pages
- Single post pages with categories and tags
- Pagination
- No external runtime dependencies

## Installation

Add the theme as a Git submodule:

```sh
git submodule add https://github.com/codertesla/hugo-paper-reader.git themes/paper-reader
```

Set the theme in `hugo.toml` or `config.toml`:

```toml
theme = "paper-reader"
```

If you clone the repository into `themes/hugo-paper-reader`, use:

```toml
theme = "hugo-paper-reader"
```

## Example Configuration

```toml
baseURL = "https://example.com/"
title = "Paper Reader"
theme = "paper-reader"
locale = "zh-cn"
defaultContentLanguage = "zh-cn"

[pagination]
  pagerSize = 10

[params]
  description = "A quiet place for reading."
  info = "Essays, notes, and observations."
  footercontent = "Made with Hugo and Paper Reader."

[taxonomies]
  category = "categories"
  tag = "tags"

[menu]
  [[menu.main]]
    name = "Home"
    url = "/"
    weight = 1

  [[menu.main]]
    name = "Posts"
    url = "/post/"
    weight = 2

  [[menu.main]]
    name = "Categories"
    url = "/categories/"
    weight = 3

  [[menu.main]]
    name = "Tags"
    url = "/tags/"
    weight = 4

  [[menu.main]]
    name = "About"
    url = "/about/"
    weight = 5
```

## Run the Example Site

From the theme repository:

```sh
hugo server --source exampleSite --themesDir ../..
```

## Content Structure

Paper Reader expects posts under `content/post/` by default. The home page lists regular pages in the `post` section.

Example front matter:

```yaml
---
title: "A Quiet Essay"
date: 2026-07-02
description: "A short description for list pages."
categories:
  - Notes
tags:
  - Hugo
  - Writing
---
```

## Customization

Override any template or static asset in your Hugo site using Hugo's standard lookup order.

The main stylesheet is:

```text
static/css/style.css
```

## License

MIT
