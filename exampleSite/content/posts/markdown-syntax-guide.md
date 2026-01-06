+++
title = "Markdown Syntax Guide"
date = 2023-11-10T09:15:00Z
draft = false
tags = ["markdown", "writing", "reference"]
slug = "markdown-syntax-guide"
+++

This post demonstrates the various markdown syntax elements that you can use in your Hugo blog posts.

<!--more-->
## Headers

# H1 Header
## H2 Header  
### H3 Header
#### H4 Header
##### H5 Header
###### H6 Header

## Emphasis

*This text will be italic*
_This will also be italic_

**This text will be bold**
__This will also be bold__

***This text will be bold and italic***

## Lists

### Unordered List

* Item 1
* Item 2
  * Item 2a
  * Item 2b

### Ordered List

1. First item
2. Second item
3. Third item
   1. Subitem 3a
   2. Subitem 3b

## Links

[Hugo Website](https://gohugo.io)

[Link with title](https://gohugo.io "Hugo Homepage")

## Images

![Alt text](https://via.placeholder.com/300x200 "Optional title")

## Code

### Inline Code

Use `hugo server` to start the development server.

### Code Blocks

```javascript
function greet(name) {
    console.log(`Hello, ${name}!`);
}

greet("World");
```

```python
def fibonacci(n):
    if n <= 1:
        return n
    return fibonacci(n-1) + fibonacci(n-2)

print(fibonacci(10))
```

## Blockquotes

> This is a blockquote.
> It can span multiple lines.
>
> > Nested blockquotes are also possible.

## Tables

| Feature | Hugo | Jekyll | Gatsby |
|---------|------|--------|--------|
| Speed   | ⚡⚡⚡ | ⚡     | ⚡⚡    |
| Learning Curve | Easy | Medium | Hard |
| Templates | Go | Liquid | React |

## Horizontal Rules

---

## Task Lists

- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media

That covers most of the markdown syntax you'll use in your blog posts!