+++
title = "Responsive Web Design Fundamentals"
date = 2023-12-20T12:00:00Z
draft = false
tags = ["css", "web-design", "responsive"]
slug = "responsive-design"
+++

Creating websites that look great on all devices is essential in modern web development.
<!--more-->

## Mobile-First Approach

Start with mobile styles, then enhance for larger screens:

```css
/* Base mobile styles */
.container {
  width: 100%;
  padding: 1rem;
}

/* Tablet and up */
@media (min-width: 768px) {
  .container {
    max-width: 720px;
    margin: 0 auto;
  }
}

/* Desktop */
@media (min-width: 1024px) {
  .container {
    max-width: 960px;
  }
}
```

## Flexible Images

```css
img {
  max-width: 100%;
  height: auto;
}
```

## Viewport Meta Tag

Always include in your HTML:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

## Common Breakpoints

- **Mobile**: < 768px
- **Tablet**: 768px - 1023px
- **Desktop**: ≥ 1024px

Test your designs on real devices when possible!
