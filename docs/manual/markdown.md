# Supported markdown syntax

This page demonstrates the supported markdonw syntax, with some extended support
through [pymdownx].

## Code blocks

=== "Markdown"
    ````markdown
    ```python
    import numpy as np

    J = - np.einsum('ij,jk->ik', Omega, X)
    ```
    ````

=== "Result"
    ```python
    import numpy as np

    J = - np.einsum('ij,jk->ik', Omega, X)
    ```

## MathJax

Following the documentation of [pymdownx][mathjax], you can include math
equations by adding the extra javascript (mathjax or katex). To do so, make the
following changes to your `mkdocs.yml` and `docs/js/mathjax.js`.

=== "Edit `mkdocs.yml`"
    ```yaml
    extra_javascript:
      - js/mathjax.js
      - https://polyfill.io/v3/polyfill.min.js?features=es6
      - https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js
    ```

=== "Create `docs/js/mathjax.js`"
    ``` javascript
    window.MathJax = {
    tex: {
        inlineMath: [ ["\\(","\\)"] ],
        displayMath: [ ["\\[","\\]"] ],
        processEscapes: true,
        processEnvironments: true
    },
    options: {
        ignoreHtmlClass: ".*",
        processHtmlClass: "arithmatex"
    }
    };
    ```

Then you can inline LaTeX equations in your documentaiton.

=== "Markdown"
    ```markdown
    $$
    -\mathbf{J} =\boldsymbol{\Omega} \mathbf{X}
    $$
    ```
=== "Result"
    $$
    -\mathbf{J} =\boldsymbol{\Omega} \mathbf{X}
    $$




## Admonition

Admonition is supported through the pymarkdown [admonition] plugin.

=== "Markdown"
    ```markdown
    !!! note
        A blue chunck of text.
    ```
=== "Result"
    !!! note
        A blue chunck of text.


[mathjax]: https://facelessuser.github.io/pymdown-extensions/extensions/arithmatex/
[pymdownx]: https://facelessuser.github.io/pymdown-extensions/
[admonition]: https://python-markdown.github.io/extensions/admonition/