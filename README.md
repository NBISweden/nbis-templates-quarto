# NBIS Quarto template

This repository contains a simple [Quarto](https://quarto.org/) template for use
in _e.g._ NBIS fee-for-service reports. Quarto works with both Python and R out
of the box, as well as for both HTML/PDF reports and revealjs-based
presentations - the current version only includes a HTML-based template,
however.

## Installation

If you've already installed Quarto you can install the template like so:

```bash
quarto use template NBISweden/nbis-templates-quarto
```

This will install the template (_i.e._ create the `_extensions/` directory in
your current location) and create an example `.qmd` file that you can use as a
starting place for your report. You can also just install the template itself
without getting the `.qmd` file like so:

```bash
quarto add NBISweden/nbis-templates-quarto
```

## Usage

After a successful installation you can use the template by specifying the
format in your YAML header, like so:

```yaml
...
format:
    nbis-html: default
...
```

The template uses the NBIS colours for _e.g._ table of contents, inline code and
others. You can check the default format specifications in the
`_extensions/nbis/_extension.yml` file, which can be overridden by your own YAML
header, like so:

```yaml
...
format:
    nbis-html:
        embed-resources: false
...
```

You can find a minimal example in the [template.qmd](_extensions/nbis/template.qmd)
file. While the example is using R and the `knitr` engine you can easily use a
Jupyter kernel instead by specifying _e.g._ `jupyter: python3` or `jupyter: r`
instead of `knitr: ...`.
