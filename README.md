# Interactive Tutorial Demo

A repository demonstrating one way to manage and distribute interactive tutorials

## Goals

- Source maintained in MyST Markdown
  - Plays well with version control
  - Supports cross-references (unlike plain Markdown)
- Executed examples published as HTML on CI
- Use can download source as Markdown, Jupyter notebooks, and plain `.py` scripts
- Easy to test examples locally, outside of the documentation build process
- Changed examples are run on CI on PR
- All examples are run fresh on scheduled CI

## Prior Art

Examples that this is drawing from:

- https://github.com/bsipocz/irsa-tutorials
- https://github.com/MotherDuck-Open-Source/sql-tutorial

## Usage

```
pixi run build
```
