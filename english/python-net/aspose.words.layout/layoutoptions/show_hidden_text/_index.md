---
title: show_hidden_text property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets indication of whether hidden text in the document is rendered"
type: docs
weight: 70
url: /python-net/aspose.words.layout/layoutoptions/show_hidden_text/
---

## LayoutOptions.show_hidden_text property

Gets or sets indication of whether hidden text in the document is rendered.
Default is ``False``.


This property affects all hidden content, not just text.


### Examples

Shows how to hide text in a rendered output document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert hidden text, then specify whether we wish to omit it from a rendered document.
builder.writeln("This text is not hidden.")
builder.font.hidden = True
builder.writeln("This text is hidden.")

doc.layout_options.show_hidden_text = show_hidden_text

doc.save(ARTIFACTS_DIR + "Document.layout_options_hidden_text.pdf")
```

### See Also

* module [aspose.words.layout](../../)
* class [LayoutOptions](../)

