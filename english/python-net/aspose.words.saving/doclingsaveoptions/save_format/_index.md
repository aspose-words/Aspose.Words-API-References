---
title: DoclingSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "DoclingSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 30
url: /python-net/aspose.words.saving/doclingsaveoptions/save_format/
---

## DoclingSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.DOCLING](../../../aspose.words/saveformat/#DOCLING).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

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

