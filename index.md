# Test

```{eval-rst}
.. admonition:: A title

   A body
```

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
make gettext
sphinx-intl update -p _build/gettext -l de
```

Then edit PO files.
