# Installation and Setup

Install the latest release through [PyPI]:

[PyPI]: https://pypi.org/project/mkdocs-flux

```bash
pip install mkdocs-flux
```

or the latest version directly through the GitHub repo:

```bash
pip install git+https://github.com/yqshao/mkdocs-flux.git
```

## Basic Setup

To start with, here is a minimal setup for a new project:

```yaml
# the span tag provides the color-swap effect
site_name: "mkdocs<span>flux</span>" 
site_url: https://yqshao.github.io/mkdocs-flux
# this gives the git icon 
repo_name: yqshao/mkdocs-flux 
repo_url: https://github.com/yqshao/mkdocs-flux
# the first-level labels will become tabs,
# the second/third becomes pages or sections
nav:
  - Home: index.md
  - Usage:
      - Setup: usage/setup.md
      - Markdown: usage/markdown.md
      - Plugins:
          - pymdownx: usage/pymdownx.md
          - bibtex: usage/bibtex.md
  - About: about.md

```

Below you find a more elaborated setup is for this website, it cover most of the
features known to work. Check individual pages to see details for each plugin.

??? Note "config for this site"

    ```yaml
    --8<-- "mkdocs.yml"
    ```

## Write your documentation

Populate your `docs` folder with a few markdown files and your should be ready
to see your documentation!

``` console
mkdocs serve
```

The rest of this documentation page has some extra examples showcasing features
supported in this theme.
