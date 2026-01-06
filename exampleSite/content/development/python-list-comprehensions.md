+++
title = "Python List Comprehensions Explained"
date = 2023-12-01T13:45:00Z
draft = false
tags = ["python", "programming", "tutorial"]
slug = "python-list-comprehensions"
+++

List comprehensions provide a concise way to create lists in Python.
<!--more-->

## Basic Syntax

Instead of writing:

```python
squares = []
for i in range(10):
    squares.append(i**2)
```

You can write:

```python
squares = [i**2 for i in range(10)]
```

## With Conditions

Filter even numbers and square them:

```python
even_squares = [i**2 for i in range(10) if i % 2 == 0]
```

## Nested Comprehensions

```python
matrix = [[i*j for j in range(5)] for i in range(5)]
```

## When to Use

- Creating new lists from existing iterables
- Filtering and transforming data
- Simple operations that fit on one line

## When NOT to Use

- Complex logic that hurts readability
- Multiple conditions that make it hard to understand
- Side effects (list comprehensions should be pure)

Keep it simple and readable!
