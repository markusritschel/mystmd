---
title: Website Templates
description: There are two templates for MyST websites, a `book-theme`, based loosely on JupyterBook, and an `article-theme` that is designed for scientific documents with supporting notebooks.
---

There are currently two templates for MyST websites, a `book-theme`, which is the default and is based loosely on JupyterBook and an `article-theme` that is designed for scientific documents with supporting notebooks. The documentation for this site is using the `book-theme`, for a demonstration of the `article-theme`, you can see [an article on finite volume](https://simpeg.xyz/tle-finitevolume).

:::::{tab-set}
::::{tab} Article Theme
:::{figure} ./images/article-theme.png
Example of a banner in a site using the `article-theme`, ([online](https://simpeg.xyz/tle-finitevolume/), [source](https://github.com/simpeg/tle-finitevolume))
:::
::::

::::{tab} Book Theme
:::{figure} ./images/book-theme.png
Example of a site using the `book-theme`, ([online](https://mystmd.org), [source](https://github.com/executablebooks/mystmd/tree/main/docs))
:::
::::
:::::

## Changing Site Templates

To change your website template from the default (`book-theme`), use the `site: template:` property:

```{code} yaml
:filename: myst.yml
:emphasize-lines: 4
:caption: Change the `template` property to `article-theme`.
:linenos:
project:
  ...
site:
  template: article-theme
```

### Article Theme

The article theme is centered around a single document with supporting content, which is how many scientific articles are structured today: a narrative article with associated computational notebooks to reproduce a figure, document data-cleaning steps, or provide interactive visualization. These are listed as "supporting documents" in this theme and can be pulled in as normal with your [](./table-of-contents.md). For information on how to import your figures into your article, see [](./reuse-jupyter-outputs.md).

The frontmatter that is displayed at the top of the article is the contents of your project, including a project [thumbnail and banner](#thumbnail-and-banner). The affiliations for your authors, their ORCID, email, etc. are available by clicking directly on the author name.

(site-options)=

## Site Options

There are a number of common options between the site templates. These should be placed in the `site.options` in your `myst.yml`.

```{code-block} yaml
:filename: myst.yml
site:
  options:
    favicon: my-favicon.ico
    logo: my-site-logo.svg
```

```{list-table} Site Options
:header-rows: 1
:label: tbl:site-options
* - option
  - description
* - `favicon`
  - a file - Local path to favicon image
* - `logo`
  - a file - Local path to logo image
* - `logo_dark`
  - a file - Local path to logo image to be used in dark mode only
* - `logo_text`
  - a string - Short text to display next to logo at the top of all pages
* - `analytics_google`
  - a string - Google analytics key, see [](./analytics.md)
* - `analytics_plausible`
  - a string - Plausible analytics key, see [](./analytics.md)
```
