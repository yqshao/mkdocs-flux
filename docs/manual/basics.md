# Basics

## Use a template

If you are creating a new repo, the easist way of use the theme is to use one of
the templates, which setups up the developer's environment with some recommended
setups, auto-building of the documentation with Github pages, and a code space.
If you'd like to manually set up mkdocs, follow the installation instruction
below, along with a commented config file.

## Installation and setup

```bash
pip install git+https://github.com/yqshao/mkdocs-flux.git
```

Put the following into your mkdocs.yml, available options are explained here

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
