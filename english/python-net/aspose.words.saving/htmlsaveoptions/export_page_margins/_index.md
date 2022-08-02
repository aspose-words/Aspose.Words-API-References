---
title: export_page_margins property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies whether page margins is exported to HTML, MHTML or EPUB"
type: docs
weight: 220
url: /python-net/aspose.words.saving/htmlsaveoptions/export_page_margins/
---

## HtmlSaveOptions.export_page_margins property

Specifies whether page margins is exported to HTML, MHTML or EPUB.
Default is ``false``.


Aspose.Words does not show area of page margins by default. 
If any elements are completely or partially clipped by the document edge the displayed area can be extended with
this option.


### Examples

Shows how to show out-of-bounds objects in output HTML documents.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Use a builder to insert a shape with no wrapping.
shape = builder.insert_shape(aw.drawing.ShapeType.CUBE, 200, 200)

shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.wrap_type = aw.drawing.WrapType.NONE

# Negative shape position values may place the shape outside of page boundaries.
# If we export this to HTML, the shape will appear truncated.
shape.left = -150

# When saving the document to HTML, we can pass a SaveOptions object
# to decide whether to adjust the page to display out-of-bounds objects fully.
# If we set the "export_page_margins" flag to "True", the shape will be fully visible in the output HTML.
# If we set the "export_page_margins" flag to "False",
# our document will display the shape truncated as we would see it in Microsoft Word.
options = aw.saving.HtmlSaveOptions()
options.export_page_margins = export_page_margins

doc.save(ARTIFACTS_DIR + "HtmlSaveOptions.export_page_margins.html", options)

with open(ARTIFACTS_DIR + "HtmlSaveOptions.export_page_margins.html", "rt", encoding="utf-8") as file:
    out_doc_contents = file.read()

if export_page_margins:
    self.assertIn("<style type=\"text/css\">div.Section1 { margin:70.85pt }</style>", out_doc_contents)
    self.assertIn("<div class=\"Section1\"><p style=\"margin-top:0pt; margin-left:151pt; margin-bottom:0pt\">", out_doc_contents)
else:
    self.assertNotIn("style type=\"text/css\">", out_doc_contents)
    self.assertIn("<div><p style=\"margin-top:0pt; margin-left:221.85pt; margin-bottom:0pt\">", out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

