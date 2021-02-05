# Test

## Test cases

```{eval-rst}
.. admonition:: A title

   A body
```

This is **bold text**.

## Reproduction

Install:

```
pip install sphinx sphinx-intl myst-parser
```

Run:

```
sphinx-build -b dirhtml . _build -D language="es"
```

BUG:

```
/path/to/index.md:4:<translated>:1: WARNING: Non-consecutive header level increase; 0 to 2
```

## Maintenance

Create PO files:

```
sphinx-build -b gettext . _build/gettext
sphinx-intl update -p _build/gettext -l es
```

Then edit PO files.
