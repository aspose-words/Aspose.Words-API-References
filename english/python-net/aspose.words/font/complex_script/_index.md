---
title: complex_script property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies whether the contents of this run shall be treated as complex script text regardless of their Unicode character values when determining the formatting for this run."
type: docs
weight: 80
url: /python-net/aspose.words/font/complex_script/
---

## Font.complex_script property

Specifies whether the contents of this run shall be treated as complex script text regardless
of their Unicode character values when determining the formatting for this run.


### Examples

Shows how to add text that is always treated as complex script.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.font.complex_script = True

builder.writeln("Text treated as complex script.")

doc.save(ARTIFACTS_DIR + "Font.complex_script.docx")
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

