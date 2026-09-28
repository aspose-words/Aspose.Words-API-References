---
title: DoclingSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "DoclingSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 30
url: /zh/python-net/aspose.words.saving/doclingsaveoptions/save_format/
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
# 设置为 true 可渲染非图像形状并将其包含在输出中。
# 设置为 false（默认）可从输出中排除非图像形状。
save_options.render_non_image_shapes = True
doc.save(file_name=ARTIFACTS_DIR + 'Document.DoclingJson.json', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [DoclingSaveOptions](../)

