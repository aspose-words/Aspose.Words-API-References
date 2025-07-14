---
title: PdfSaveOptions.export_paragraph_graphics_to_artifact property
linktitle: export_paragraph_graphics_to_artifact property
articleTitle: export_paragraph_graphics_to_artifact property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.export_paragraph_graphics_to_artifact property. Gets or sets a value determining whether a paragraph graphic should be marked as an artifact."
type: docs
weight: 160
url: /python-net/aspose.words.saving/pdfsaveoptions/export_paragraph_graphics_to_artifact/
---

## PdfSaveOptions.export_paragraph_graphics_to_artifact property

Gets or sets a value determining whether a paragraph graphic should be marked as an artifact.


```python
@property
def export_paragraph_graphics_to_artifact(self) -> bool:
    ...

@export_paragraph_graphics_to_artifact.setter
def export_paragraph_graphics_to_artifact(self, value: bool):
    ...

```

### Remarks

Default value is ``False`` and paragraph graphics (underlines, text emphasis, etc.)
will be marked as "Span" in the logical structure of the document.

When the value is ``True`` the paragraph graphics will be marked as "Artifact".

This value is ignored when [PdfSaveOptions.export_document_structure](../export_document_structure/) is ``False``. 




### Examples

Shows how to export paragraph graphics as artifact (underlines, text emphasis, etc.).

```python
doc = aw.Document(file_name=MY_DIR + 'PDF artifacts.docx')
save_options = aw.saving.PdfSaveOptions()
save_options.export_document_structure = True
save_options.export_paragraph_graphics_to_artifact = True
save_options.text_compression = aw.saving.PdfTextCompression.NONE
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportParagraphGraphicsToArtifact.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

