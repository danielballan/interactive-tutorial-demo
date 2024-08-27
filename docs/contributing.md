# Contributing

First, clone this repository.

With HTTPS:

```sh
git clone https://github.com/danielballan/interactive-tutorial-demo
```

With SSH:
```sh
git clone git@github.com:danielballan/interactive-tutorial-demo
```

We use the [pixi](https://pixi.sh/latest/#installation) package manager to
create an environment with dependencies from conda-forge and PyPI. We recommend
installing pixi. But if you have a strong preference for a different package
manager, peek inside `pixi.toml` to find the list of dependencies and install
them however you wish.

## Build

```sh
pixi run build
```

```{note}
Later, if the build results get into a broken state, use `pixi run clean`
to start fresh.
```

This creates:
- Executed notebooks under `build/juptyer_execute/`
- HTML under `build/html/`.

Open `build/html/index.html` in a web browser.

## Develop

```
pixi run jupyter lab
```

In the file browser, locate one of the examples under `docs/recipes/`. Double
click to open.

Files like `docs/recipes/static/static.md` are plain Markdown files. Files like
`docs/recipes/executable/basics.md` have a special header which enables the
documentation build system to convert them to Jupyter notebooks and execute
them:

```yaml
---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.16.4
kernelspec:
  display_name: Python 3 (ipykernel)
  language: python
  name: python3
---
```

Jupyter Lab can open these files _as notebooks_ enabling you the interactively
edit and execute them, saving the changes to Markdown.

![Context Menu: Open With... Jupytext Notebook](./_static/images/open-with-jupytext-notebook.png)

Note that the cell _outputs_ are not saved to disk. This is a feature, not a
bug. The inputs are stored a in version-control friendly textual format
(Markdown). This is converted to Jupyter notebook format and executed during
the build process.
