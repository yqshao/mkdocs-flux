# BibTeX support

Basic referencing with the `[@bib_key]` syntax is possible.[@1931_Onsager]
You'll need the [mkdocs-bibtex] plugin, and add the following to your
`mkdocs.yml`:

```yaml
plugins:
  - bibtex:
      bib_file: "docs/refs.bib"
```

By default, the references show up as footnotes at the end of pages.

[mkdocs-bibtex]: https://github.com/shyamd/mkdocs-bibtex/