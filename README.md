# Dola, a Zola theme

[Zola](https://www.getzola.org/) is a static site generator that is similar to [Hugo](https://gohugo.io/) but written in Rust.

This repository contains a theme that is intended for use as follows:

 - The `content/_index.md` contains your home page.
 - Additional sections can be created by adding a directory to `content`, for example, `content/projects/`; each directory can then be added as a new section on navigation bar, and each page within will be displayed using a grid of cards.
 - Pages can be added to a section by creating a new markdown file in that section's directory, for example, `content/projects/my-first-project.md`.

## Instructions for use

1. Initialise your site [using Zola](https://www.getzola.org/documentation/getting-started/overview/#initialize-site).
1. Remove all content generated except the `content` and `themes` directories, and the `config.toml` file.
1. `cd` into themes and `git clone` this repository.
1. `cd` back into your site directory and copy the example content files using `cp -r themes/dola/content content`/
1. Set your site to use this theme by adding `theme = "dola"` to the top of your `config.toml`.

## Customisation using `config.toml`

Further customisation can be done by adding entries under `[extra]` in `config.toml`.

## Title

Set the title by creating a `title` variable:

```toml
title = "my-title"
```

### Navigation bar

Add items to the navbar by creating a `navbar` variable:

```toml
navbar = [
    {url = "BASE_URL", name = "Home"},
    {url = "BASE_URL/projects/", name = "Projects"},
]
```

### Footer contact details

Add your contact details to the footer by creating a `contacts` variable:

```toml
contacts = [{icon = "fab fa-github", link = "https://github.com/dancs-dev"}, {icon = "fas fa-envelope", link = "mailto:email@example.com"}]
```

