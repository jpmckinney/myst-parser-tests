# Test

## Test cases

### Admonition

```{eval-rst}
.. admonition:: A title

   A body
```

### CSV Table

```{csv-table}
   :header-rows: 1
   :file: codelist.csv
```

### Math

If Alice gives Bob $10, and Bob gives Eve $10, how much money does Bob have?

## Reproduction

Install:

```
pip install sphinx sphinx-intl myst-parser
```

Create PO files:

```
sphinx-build -b gettext . _build/gettext
sphinx-intl update -p _build/gettext -l es
```

Build HTML pages:

```
sphinx-build -b dirhtml . _build -D language="es"
```

BUG: `/path/to/index.md:4:<translated>:1: WARNING: Non-consecutive header level increase; 0 to 2`
