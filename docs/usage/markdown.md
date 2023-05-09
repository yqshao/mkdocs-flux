# Basic markdown syntax

The following markdown syntax should be supported with a default mkdocs
installation. More features are avaialable the plugins section.

## Admonition

Admonition is supported through the [admonition] plugin. Admonition can have
custom types, but only three types: `note`, `warning`, and `danger` have
configured colors in mkdocs-flux.

[admonition]: https://python-markdown.github.io/extensions/admonition/

=== "Markdown"

    ```Markdown
    !!! Note

        A blue chunck of text.

    --- 

    !!! Warning
    
        A yellow chunck of text.

    --- 

    !!! Danger

        A red chunck of text.

    --- 

    !!! Default

        A gray chunck of text.
    ```

=== "Result"

    !!! Note

        A blue chunck of text.

    --- 

    !!! Warning
    
        A yellow chunck of text.

    --- 

    !!! Danger

        A red chunck of text.

    --- 

    !!! Default

        A gray chunck of text.
