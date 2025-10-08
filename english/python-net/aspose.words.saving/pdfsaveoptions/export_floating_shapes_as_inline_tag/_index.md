---
title: PdfSaveOptions.export_floating_shapes_as_inline_tag property
linktitle: export_floating_shapes_as_inline_tag property
articleTitle: export_floating_shapes_as_inline_tag property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.export_floating_shapes_as_inline_tag property. Gets or sets a value determining whether floating shapes are exported as inline tags in the document structure."
type: docs
weight: 150
url: /python-net/aspose.words.saving/pdfsaveoptions/export_floating_shapes_as_inline_tag/
---

## PdfSaveOptions.export_floating_shapes_as_inline_tag property

Gets or sets a value determining whether floating shapes are exported as inline tags in the document structure.


```python
@property
def export_floating_shapes_as_inline_tag(self) -> bool:
    ...

@export_floating_shapes_as_inline_tag.setter
def export_floating_shapes_as_inline_tag(self, value: bool):
    ...

```

### Remarks

Default value is ``False`` and floating shapes will be exported as block-level tags,
placed after the paragraph in which they are anchored.

When the value is ``True`` floating shapes will be exported as inline tags,
placed within the paragraph where they are anchored.

This value is ignored when [PdfSaveOptions.export_document_structure](../export_document_structure/) is ``False``. 




### Examples

Shows how to export floating shapes as inline tags.

```python
doc = aw.Document(file_name=MY_DIR + 'Floating object.docx')
save_options = aw.saving.PdfSaveOptions()
save_options.export_floating_shapes_as_inline_tag = True
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportFloatingShapesAsInlineTag.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

