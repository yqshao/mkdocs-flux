# BibTeX support

!!! warning

    As of Apr. 2023 (mkdocs-bibtex v2.8.16) there is a known [issue] of
    mkdocs-bibtex overwriting existing footnotes. Change your footnote keys if
    this happens.

Basic referencing is possible. You'll need the [mkdocs-bibtex] plugin, and add
the following to your `mkdocs.yml`:

```yaml
plugins:
  - bibtex:
      bib_file: "docs/refs.bib"
      csl_file: "docs/jcp.csl"
```

References show up as footnotes at the end of the page like this.[@1931_Onsager]
The pandoc syntax `[@bib_key]` applies, and the citation style can be changed
with the `csl_file` option. However, advanced features like locator or suffix
do not seem to work so far.

[issue]: https://github.com/shyamd/mkdocs-bibtex/issues/173
[mkdocs-bibtex]: https://github.com/shyamd/mkdocs-bibtex/
