---
title: Range.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "Range.text property. Gets the text of the range."
type: docs
weight: 60
url: /python-net/aspose.words/range/text/
---

## Range.text property

Gets the text of the range.


```python
@property
def text(self) -> str:
    ...

```

### Remarks

The returned string includes all control and special characters as described in [ControlChar](../../controlchar/).




### Examples

Shows how to get the text contents of all the nodes that a range covers.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.write("Hello world!")

self.assertEqual("Hello world!", doc.range.text.strip())
```

### See Also

* module [aspose.words](../../)
* class [Range](../)

