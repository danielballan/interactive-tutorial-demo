# Interactive Tutorial Demo

A repository demonstrating one way to manage and distribute interactive tutorials


## Overview

- Each recipe has a directory, named like `docs/recipes/<recipe name>`.
- Each directory contains Markdown and any supporting files: data files,
  illustrations, solutions, supporting scripts....
- The Markdown may be vanilla (CommonMark) Markdown or MyST Markdown.
  It may have a header indicating that it contains code blocks that are
  executable by a Jupyter kernel.
- From these sources, a task-runner can build:
  - HTML static site
  - executed notebooks (for the subset of recipes that contain executable Markdown)
- A GitHub Actions workflow publishes the HTML and the executed notebooks.

## TO DO

- Test notebook execution (of changed recipes only) in CI on PR.
- Test notebook execution (of all recipes) in CI on a schedule.

## Demo Links

- **[Published web pages](https://danielballan.github.io/interactive-tutorial-demo/)** --- a static site published with GitHub Pages
- **[Executed notebooks](https://github.com/danielballan/interactive-tutorial-demo/tree/notebooks)** --- published to the `notebooks` branch of this repo
- **[Binder](https://mybinder.org/v2/gh/danielballan/interactive-tutorial-demo/notebooks)**

## Goals

- Source maintained in MyST Markdown, primarily because it:
  - Plays well with version control (unlike notebooks)
  - Supports cross-references (unlike plain Markdown)
- Executed examples are published as HTML
- Examples, converted to `.ipynb` format, are published for use with Binder and/or Jupyter Lite
- Easy to test examples locally, outside of the documentation build process
- Changed examples are run on CI on PR
- All examples are run fresh on scheduled CI

## Prior Art

Examples that this is drawing from:

- https://github.com/bsipocz/irsa-tutorials
- https://github.com/MotherDuck-Open-Source/sql-tutorial

## Local Development

```
pixi run build
```
