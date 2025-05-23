﻿---
title: HtmlSaveOptions.export_page_margins property
linktitle: export_page_margins property
articleTitle: export_page_margins property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.export_page_margins property. Specifies whether page margins is exported to HTML, MHTML or EPUB"
type: docs
weight: 210
url: /python-net/aspose.words.saving/htmlsaveoptions/export_page_margins/
---

## HtmlSaveOptions.export_page_margins property

Specifies whether page margins is exported to HTML, MHTML or EPUB.
Default is ``False``.



```python
@property
def export_page_margins(self) -> bool:
    ...

@export_page_margins.setter
def export_page_margins(self, value: bool):
    ...

```

### Remarks

Aspose.Words does not show area of page margins by default.
If any elements are completely or partially clipped by the document edge the displayed area can be extended with
this option.


### Examples

Shows how to show out-of-bounds objects in output HTML documents.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Use a builder to insert a shape with no wrapping.
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.CUBE, width=200, height=200)
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.wrap_type = aw.drawing.WrapType.NONE
# Negative shape position values may place the shape outside of page boundaries.
# If we export this to HTML, the shape will appear truncated.
shape.left = -150
# When saving the document to HTML, we can pass a SaveOptions object
# to decide whether to adjust the page to display out-of-bounds objects fully.
# If we set the "ExportPageMargins" flag to "true", the shape will be fully visible in the output HTML.
# If we set the "ExportPageMargins" flag to "false",
# our document will display the shape truncated as we would see it in Microsoft Word.
options = aw.saving.HtmlSaveOptions()
options.export_page_margins = export_page_margins
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.ExportPageMargins.html', save_options=options)
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlSaveOptions.ExportPageMargins.html')
if export_page_margins:
    self.assertTrue('<style type="text/css">div.Section_1 { margin:70.85pt }</style>' in out_doc_contents)
    self.assertTrue('<div class="Section_1"><p style="margin-top:0pt; margin-left:150pt; margin-bottom:0pt">' in out_doc_contents)
else:
    self.assertFalse('style type="text/css">' in out_doc_contents)
    self.assertTrue('<div><p style="margin-top:0pt; margin-left:220.85pt; margin-bottom:0pt">' in out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

