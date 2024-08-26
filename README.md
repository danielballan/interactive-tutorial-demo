# Interactive Tutorial Demo

A repository demonstrating one way to manage and distribute interactive tutorials

## Demo

- **[Published web pages](https://danielballan.github.io/interactive-tutorial-demo/)** --- a static HTML site

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
