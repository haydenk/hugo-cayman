+++
title = "Getting Started with Hugo"
date = 2023-11-05T15:30:00Z
draft = false
tags = ["hugo", "tutorial", "static-site"]
slug = "getting-started-with-hugo"
+++

Hugo is one of the fastest static site generators available today. In this post, I'll walk you through the basics of getting started with Hugo.
<!--more-->

## Installation

Installing Hugo is straightforward. On macOS, you can use Homebrew:

```bash
brew install hugo
```

For other platforms, check the [official Hugo documentation](https://gohugo.io/getting-started/installing/).

## Creating Your First Site

Once Hugo is installed, creating a new site is simple:

```bash
hugo new site my-blog
cd my-blog
```

## Directory Structure

Hugo follows a specific directory structure:

- `content/` - Your markdown content files
- `layouts/` - HTML templates
- `static/` - Static assets (CSS, JS, images)
- `config.toml` - Site configuration

## Adding Content

To create a new post:

```bash
hugo new posts/my-first-post.md
```

This will create a new markdown file with front matter already set up.

## Running the Development Server

To preview your site locally:

```bash
hugo server -D
```

The `-D` flag includes draft content in the build.

## Building for Production

When you're ready to deploy:

```bash
hugo
```

This generates the static site in the `public/` directory.

## Next Steps

Now that you have the basics down, you can:

- Explore themes
- Customize layouts
- Add shortcodes
- Configure menus and navigation

Happy blogging with Hugo!