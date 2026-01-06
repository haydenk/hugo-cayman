+++
title = "Frontend Performance Optimization Techniques"
date = 2024-01-20T10:00:00Z
draft = false
tags = ["performance", "web-development", "optimization"]
slug = "performance-optimization"
+++

Slow websites lose users. Here's how to make your web apps blazingly fast.
<!--more-->

## Measure First

Use tools to identify bottlenecks:
- Chrome DevTools Performance tab
- Lighthouse
- WebPageTest
- Core Web Vitals

## Code Splitting

Load only what you need:

```javascript
// Instead of
import HeavyComponent from './HeavyComponent';

// Use dynamic imports
const HeavyComponent = lazy(() => import('./HeavyComponent'));
```

## Image Optimization

```html
<!-- Use modern formats -->
<picture>
  <source srcset="image.webp" type="image/webp">
  <source srcset="image.jpg" type="image/jpeg">
  <img src="image.jpg" alt="Description" loading="lazy">
</picture>
```

## Lazy Loading

```javascript
// Intersection Observer for lazy loading
const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.src = entry.target.dataset.src;
      observer.unobserve(entry.target);
    }
  });
});
```

## Caching Strategies

```javascript
// Service Worker caching
self.addEventListener('fetch', (event) => {
  event.respondWith(
    caches.match(event.request)
      .then(response => response || fetch(event.request))
  );
});
```

## Minification & Compression

- Minify JavaScript and CSS
- Enable gzip/brotli compression
- Remove unused code
- Tree shake dependencies

## Key Metrics

- **FCP**: First Contentful Paint < 1.8s
- **LCP**: Largest Contentful Paint < 2.5s
- **CLS**: Cumulative Layout Shift < 0.1
- **FID**: First Input Delay < 100ms

Every millisecond counts!
