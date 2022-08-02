---
title: underline property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets/sets underline type for the current font."
type: docs
weight: 170
url: /python-net/aspose.words/documentbuilder/underline/
---

## DocumentBuilder.underline property

Gets/sets underline type for the current font.


### Examples

Shows how to format text inserted by a document builder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.underline = aw.Underline.DASH
builder.font.color = drawing.Color.blue
builder.font.size = 32

# The builder applies formatting to its current paragraph and any new text added by it afterward.
builder.writeln("Large, blue, and underlined text.")

doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_underline.docx")
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

