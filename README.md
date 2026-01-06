# Hugo Cayman Theme

A clean, responsive Hugo theme converted from the [Jekyll Cayman theme](https://github.com/pages-themes/cayman). Features a bold gradient header, responsive design, and automatic dark mode support.

## Features

- Clean, minimal design
- Responsive layout
- Automatic dark mode using CSS `light-dark()` function
- Syntax highlighting with Hugo Chroma (github and github-dark styles)
- CSS-only (no Sass preprocessing required)
- Modular CSS architecture for easy customization
- SEO-friendly with Open Graph meta tags
- Font optimization with preconnect and preload

## Installation

### As a Hugo Module (Recommended)

1. Initialize your Hugo site as a module:

   ```bash
   hugo mod init github.com/yourusername/yoursite
   ```

2. Add the theme to your `config.toml`:

   ```toml
   [module]
     [[module.imports]]
       path = "github.com/haydenk/hugo-cayman"
   ```

3. Update modules:

   ```bash
   hugo mod get -u
   ```

### As a Git Submodule

```bash
cd your-hugo-site
git submodule add https://github.com/haydenk/hugo-cayman.git themes/cayman
```

Then add to your `config.toml`:

```toml
theme = "cayman"
```

### Manual Installation

1. Download or clone this repository into your `themes/` directory
2. Add `theme = "cayman"` to your `config.toml`

## Configuration

Example `config.toml`:

```toml
baseURL = "https://example.com/"
languageCode = "en-us"
title = "My Hugo Site"
theme = "cayman"

[params]
  description = "A clean, responsive Hugo site"
  tagline = "Your site tagline here"
  author = "Your Name"

  [params.home]
      post_limit = 10

  # GitHub integration (optional)
  [params.github]
    repository_url = "https://github.com/username/repo"
    repository_name = "repo"
    owner_url = "https://github.com/username"
    owner_name = "username"
    is_project_page = true
    zip_url = "https://github.com/username/repo/zipball/main"
    tar_url = "https://github.com/username/repo/tarball/main"

  # Show download buttons (requires github URLs above)
  show_downloads = false

  # Custom footer text (optional)
  footer_text = "Your custom footer text here"

# Syntax highlighting configuration
[markup]
  [markup.highlight]
    lineNos = false
    noClasses = false

# Main sections (for homepage post listing)
[params]
  mainSections = ["posts", "blog"]
```

## Content Structure

Create content using TOML frontmatter:

```toml
+++
title = "My First Post"
date = 2026-01-05
draft = false
description = "A brief description of this post"
+++

Your content here...
```

## Customization

### CSS Variables

The theme uses CSS custom properties for easy customization. Override them by creating a custom CSS file in your site's `assets/css/` directory:

```css
:root {
  --header-bg-color: light-dark(#159957, #115740);
  --header-bg-color-secondary: light-dark(#155799, #0d3a66);
  --section-headings-color: light-dark(#159957, #4ade80);
  --body-text-color: light-dark(#606c71, #c9d1d9);
  --body-link-color: light-dark(#1e6bb8, #58a6ff);
}
```

### Dark Mode

The theme automatically switches between light and dark modes based on the user's system preference using the CSS `light-dark()` function. Syntax highlighting also adapts automatically.

### Custom Layouts

Override any template by creating the same file path in your site's `layouts/` directory. For example:

- `layouts/_default/baseof.html` - Base template
- `layouts/partials/header.html` - Page header
- `layouts/partials/footer.html` - Page footer

## Directory Structure

```text
hugo-cayman/
├── archetypes/
│   └── default.md           # TOML frontmatter template
├── assets/
│   └── css/
│       ├── _variables.css   # CSS custom properties
│       ├── _font.css        # Font CSS Settings
│       ├── _syntax.css      # Hugo chroma styles light and dark
│       ├── _normalize.css   # Normalize.css
│       └── main.css         # Theme styles
├── layouts/
│   ├── _default/
│   │   ├── baseof.html      # Base template
│   │   ├── single.html      # Single page template
│   │   └── list.html        # List page template
│   ├── partials/
│   │   ├── head.html        # Head section
│   │   ├── head/
│   │   │   ├── css.html     # CSS asset bundling
│   │   │   └── js.html      # JS asset bundling
│   │   ├── header.html      # Page header
│   │   └── footer.html      # Footer
│   └── index.html           # Homepage template
├── LICENSE
├── README.md
└── theme.toml
```

## Development

The theme uses Hugo's asset pipeline to combine and minify CSS files. In development mode, files are served separately for easier debugging. In production, they're combined and minified automatically.

Run your site in development:

```bash
mise serve
```

Build for production:

```bash
mise build
```

## Credits

- Original [Cayman theme](https://github.com/pages-themes/cayman) by GitHub
- Converted to Hugo with modern CSS features
- Uses [Normalize.css](https://necolas.github.io/normalize.css/)
- Font: [Open Sans](https://fonts.google.com/specimen/Open+Sans)

## License

CC0-1.0 (Public Domain)

See [LICENSE](LICENSE) for details.
