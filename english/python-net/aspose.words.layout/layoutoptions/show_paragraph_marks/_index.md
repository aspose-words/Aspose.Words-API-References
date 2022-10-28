---
title: show_paragraph_marks property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets indication of whether paragraph marks are rendered"
type: docs
weight: 80
url: /python-net/aspose.words.layout/layoutoptions/show_paragraph_marks/
---

## LayoutOptions.show_paragraph_marks property

Gets or sets indication of whether paragraph marks are rendered.
Default is ``False``.



### Examples

Shows how to show paragraph marks in a rendered output document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Add some paragraphs, then enable paragraph marks to show the ends of paragraphs
# with a pilcrow (¶) symbol when we render the document.
builder.writeln("Hello world!")
builder.writeln("Hello again!")

doc.layout_options.show_paragraph_marks = show_paragraph_marks

doc.save(ARTIFACTS_DIR + "Document.layout_options_paragraph_marks.pdf")
```

### See Also

* module [aspose.words.layout](../../)
* class [LayoutOptions](../)

