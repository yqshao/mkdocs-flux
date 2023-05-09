# PyMarkdown Extensions

[PyMarkdown extensions][pymdownx] contain a wide selection of extensions to the
markdown syntax. Below are list of tested features, along with short
demonstrations of their setup and usage.

[pymdownx]: https://facelessuser.github.io/pymdown-extensions/

## Math equation

Following the pymdownx [documentation][mathjax], you can include math equations
by adding the extra javascript (mathjax or katex). The following example uses
mathjax:

[mathjax]: https://facelessuser.github.io/pymdown-extensions/extensions/arithmatex/

=== "mkdocs.yml"
    ```yaml
    extra_javascript:
      - js/mathjax.js
      - https://polyfill.io/v3/polyfill.min.js?features=es6
      - https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js
    ```

=== "docs/js/mathjax.js"
    ```javascript
    --8<-- "docs/js/mathjax.js"
    ```

=== "Markdown"

    ```markdown
    $$
    -\mathbf{J} =\boldsymbol{\Omega} \mathbf{X}
    $$
    ```
    
=== "Result"
    
    $$-\mathbf{J} =\boldsymbol{\Omega} \mathbf{X}$$

## Code highlight

=== "mkdocs.yml"

     ```yaml
     markdown_extensions:
       - pymdownx.superfences
       - pymdownx.highlight
     ```

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

## Task Lists

=== "mkdocs.yml"

    ```yaml
    markdown_extensions:
      - pymdownx.tasklist:
          custom_checkbox: true
          clickable_checkbox: true
    ```

=== "Markdown"

    ```markdown
    - [X] item 1
        * [X] item A
        * [ ] item B
            more text
            + [x] item a
            + [ ] item b
            + [x] item c
        * [X] item C
    - [ ] item 2
    - [ ] item 3
    ```

=== "Result"

    - [X] item 1
        * [X] item A
        * [ ] item B
            more text
            + [x] item a
            + [ ] item b
            + [x] item c
        * [X] item C
    - [ ] item 2
    - [ ] item 3
    
## Details

Details (collapsable boxes) are supported by the details plugin, the coloring
scheme is the same as [admonitons](../markdown#admonition).
=== "mkdocs.yml"

    ```yaml
    markdown_extensions:
      - pymdownx.details
    ```

=== "Markdown"

    ```markdown
    ???+ Note "Click me to close"
    
        Nagging.
    
    ---
    
    ??? Warning "Click me to open"
    
        Superise.
    ```

=== "Result"

    ???+ Note "Click me to close"
    
        Nagging.
    
    ---
    
    ??? Warning "Click me to open"
    
        Surprise.

