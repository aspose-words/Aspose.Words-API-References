---
title: DoclingSaveOptions.render_non_image_shapes property
linktitle: render_non_image_shapes property
articleTitle: render_non_image_shapes property
second_title: Aspose.Words for Python
description: "DoclingSaveOptions.render_non_image_shapes property. Gets or sets a value indicating whether non-image shapes should be rendered and written to the output Docling JSON document."
type: docs
weight: 20
url: /python-net/aspose.words.saving/doclingsaveoptions/render_non_image_shapes/
---

## DoclingSaveOptions.render_non_image_shapes property

Gets or sets a value indicating whether non-image shapes should be rendered and written to the output
Docling JSON document.


```python
@property
def render_non_image_shapes(self) -> bool:
    ...

@render_non_image_shapes.setter
def render_non_image_shapes(self, value: bool):
    ...

```

### Remarks

If the property is **false**, non-image shapes are not exported to the output document.
The default value is **false**.



### Examples

Shows how to save a document into a Docling JSON format.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
save_options = aw.saving.DoclingSaveOptions()
save_options.save_format = aw.SaveFormat.DOCLING
# Set to true to render non-image shapes and include them in the output.
# Set to false (default) to exclude non-image shapes from the output.
save_options.render_non_image_shapes = True
doc.save(file_name=ARTIFACTS_DIR + 'DoclingSaveOptions.DoclingJson.json', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [DoclingSaveOptions](../)

