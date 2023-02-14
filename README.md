# compact-pdf Quarto Format

A Quarto format for compact PDF documents. Good for short reports, homework assignments, etc.

## Example

![](thumbnail.png | width=100)

[[Source code](template.qmd)]

## Installation

```bash
quarto use template arcruz0/quarto-compact
```

This will install the extension and create a .qmd file for you to edit.

## Usage

When creating a Quarto document, simply use the "compact-pdf" format instead of "pdf". All [PDF options](https://quarto.org/docs/reference/formats/pdf.html) should work. For example:

```yaml
---
title: "My Title"
author: "My Name"
date: today
format: compact-pdf
---
```
