---
title: HtmlSaveOptions.export_shapes_as_svg property
linktitle: export_shapes_as_svg property
articleTitle: export_shapes_as_svg property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.export_shapes_as_svg property. Controls whether [Shape](../../../aspose.words.drawing/shape/) nodes are converted to SVG images when saving to HTML, MHTML, EPUB or AZW3"
type: docs
weight: 250
url: /python-net/aspose.words.saving/htmlsaveoptions/export_shapes_as_svg/
---

## HtmlSaveOptions.export_shapes_as_svg property

Controls whether [Shape](../../../aspose.words.drawing/shape/) nodes are converted to SVG images when saving
to HTML, MHTML, EPUB or AZW3.
Default value is ``False``.



```python
@property
def export_shapes_as_svg(self) -> bool:
    ...

@export_shapes_as_svg.setter
def export_shapes_as_svg(self, value: bool):
    ...

```

### Remarks

If this option is set to ``True``, [Shape](../../../aspose.words.drawing/shape/) nodes are exported as \<svg\> elements.
Otherwise, they are rendered to bitmaps and are exported as \<img\> elements.





### Examples

Shows how to export shape as scalable vector graphics.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
text_box = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=100, height=60)
builder.move_to(text_box.first_paragraph)
builder.write('My text box')
# When we save the document to HTML, we can pass a SaveOptions object
# to determine how the saving operation will export text box shapes.
# If we set the "ExportTextBoxAsSvg" flag to "true",
# the save operation will convert shapes with text into SVG objects.
# If we set the "ExportTextBoxAsSvg" flag to "false",
# the save operation will convert shapes with text into images.
options = aw.saving.HtmlSaveOptions()
options.export_shapes_as_svg = export_shapes_as_svg
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.ExportTextBox.html', save_options=options)
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlSaveOptions.ExportTextBox.html')
if export_shapes_as_svg:
    self.assertTrue('<span style="-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline">' + '<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" width="133" height="80">' in out_doc_contents)
else:
    self.assertTrue('<p style="margin-top:0pt; margin-bottom:0pt">' + '<img src="HtmlSaveOptions.ExportTextBox.001.png" width="136" height="83" alt="" ' + 'style="-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline" />' + '</p>' in out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

