# compact-pdf Quarto Format

A Quarto format for compact PDF documents. Good for short reports, homework assignments, etc.

## Example

<a href="template.pdf"><img src="thumbnail.png" width=50% height=50%></a>

[[Source code](template.qmd)]

## Installation and usage

To add the format *to a project* (Quarto extensions cannot be installed globally):

```bash
quarto add arcruz0/quarto-compact
```

Next, simply use the `compact-pdf` format instead of `pdf` in your Quarto documents. For example:

``` yaml
---
title: "My Title"
author: "My Name"
date: today
format: compact-pdf
---
```

## Details

All [PDF options](https://quarto.org/docs/reference/formats/pdf.html) should work as in the "pdf" format.

To replicate the format without installing it, just copy-paste the following into your Quarto document's YAML:

``` yaml
format: 
  pdf:
      toc: false
      shift-heading-level-by: 2
      fig-pos: "H"
      fig-cap-location: top
      geometry:
        - top=1in
        - right=.8in
        - bottom=1in
        - left=.8in
      link-citations: yes
      linkcolor: blue
      include-in-header: 
        text: |
          \usepackage{fancyhdr}
          \usepackage{titling}
          \pagestyle{fancy}
          \fancyhf{}
          \renewcommand\maketitle{
            \fancyhead[C]{
              \thetitle
              \ifx \theauthor\empty  \else \ – \theauthor \fi
              \ifx \thedate\empty  \else \ – \thedate \ \fi
            }
          }
          \fancyfoot[C]{\thepage}
```
