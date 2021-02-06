# Test

## Test cases

```{eval-rst}
.. admonition:: A title

   A body
```

### This is _italic text_

This is **bold text**.

> More **bold**

1. I am **bold**

* This is **bold**

definition
: **bold** is correct

    **Bold** indent

<div markdown=1>

**Bold** yet?

</div>

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

BUG: `_build/gettext/index.pot` contains `This is bold text` instead of `This is **bold text**.`

Build HTML pages:

```
sphinx-build -b dirhtml . _build -D language="es"
```

BUG: `/path/to/index.md:4:<translated>:1: WARNING: Non-consecutive header level increase; 0 to 2`
