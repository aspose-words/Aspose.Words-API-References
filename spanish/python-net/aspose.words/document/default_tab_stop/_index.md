---
title: Document.default_tab_stop property
linktitle: default_tab_stop property
articleTitle: default_tab_stop property
second_title: Aspose.Words for Python
description: "Document.default_tab_stop property. Gets or sets the interval (in points) between the default tab stops."
type: docs
weight: 100
url: /es/python-net/aspose.words/document/default_tab_stop/
---

## Document.default_tab_stop property

Gets or sets the interval (in points) between the default tab stops.


```python
@property
def default_tab_stop(self) -> float:
    ...

@default_tab_stop.setter
def default_tab_stop(self, value: float):
    ...

```

### Examples

Shows how to set a custom interval for tab stop positions.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Establezca tabulaciones para que aparezcan cada 72 puntos (1 pulgada).
builder.document.default_tab_stop = 72
# Cada carácter de tabulación ajusta el texto posterior a la posición de tabulación más cercana.
builder.writeln('Hello' + aw.ControlChar.TAB + 'World!')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)
* class [TabStopCollection](../../tabstopcollection/)
* class [TabStop](../../tabstop/)

