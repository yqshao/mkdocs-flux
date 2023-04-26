# Installation and Setup

## Installation

```bash
pip install git+https://github.com/yqshao/mkdocs-flux.git
```

## Basic Setup

```yaml
site_name: "mkdocs<span>flux</span>" # the <span> part changes color on hover

nav:
  - Home: index.md
  - Manual:
    - Baics: manual/basics.md
    - MathJax: manual/mathjax.md
  - About: about.md

theme:
    name: flux

markdown_extensions:
  - pymdownx.highlight:
      linenums: true
  - pymdownx.superfences
  - pymdownx.arithmatex:
      generic: true

extra_javascript:
  - javascripts/mathjax.js
  - https://polyfill.io/v3/polyfill.min.js?features=es6
  - https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js

# When the repo link is set, a github icon is displayed on top right
repo_url: https://github.com/yqshao/mkdocs-flux
repo_name: mkdocs-flux
```

## Write your documentation

Populate your `docs` folder with a few markdown files and your should be ready
to see your documentation!

``` console
mkdocs serve
```

The rest of this documentation page has some extra examples showcasing features
supported in this theme.
