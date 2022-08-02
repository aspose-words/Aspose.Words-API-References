---
title: page_color property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the page color of the document"
type: docs
weight: 50
url: /python-net/aspose.words/documentbase/page_color/
---

## DocumentBase.page_color property

Gets or sets the page color of the document. This property is a simpler version of [DocumentBase.background_shape](../background_shape/).


This property provides a simple way to specify a solid page color for the document.
Setting this property creates and sets an appropriate [DocumentBase.background_shape](../background_shape/).

If the page color is not set (e.g. there is no background shape in the document) returns 
System.Drawing.Color.Empty.




### Examples

Shows how to set the background color for all pages of a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln("Hello world!")

doc.page_color = drawing.Color.light_gray

doc.save(ARTIFACTS_DIR + "DocumentBase.set_page_color.docx")
```

### See Also

* module [aspose.words](../../)
* class [DocumentBase](../)
* property [DocumentBase.background_shape](../background_shape/)

