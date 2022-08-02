---
title: TAB_CHAR property
second_title: Aspose.Words for Python via .NET API Reference
description: "Tab character: (char)9 or \\t."
type: docs
weight: 280
url: /python-net/aspose.words/controlchar/TAB_CHAR/
---

## ControlChar.TAB_CHAR property

Tab character: (char)9 or "\\t".


### Examples

Shows how to set a custom interval for tab stop positions.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Set tab stops to appear every 72 points (1 inch).
builder.document.default_tab_stop = 72

# Each tab character snaps the text after it to the next closest tab stop position.
builder.writeln("Hello" + aw.ControlChar.TAB + "World!")
```

### See Also

* module [aspose.words](../../)
* class [ControlChar](../)

