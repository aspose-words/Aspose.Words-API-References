---
title: PdfSaveOptions.attachments_embedding_mode property
linktitle: attachments_embedding_mode property
articleTitle: attachments_embedding_mode property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.attachments_embedding_mode property. Gets or sets a value determining how attachments are embedded to the PDF document."
type: docs
weight: 30
url: /python-net/aspose.words.saving/pdfsaveoptions/attachments_embedding_mode/
---

## PdfSaveOptions.attachments_embedding_mode property

Gets or sets a value determining how attachments are embedded to the PDF document.


```python
@property
def attachments_embedding_mode(self) -> aspose.words.saving.PdfAttachmentsEmbeddingMode:
    ...

@attachments_embedding_mode.setter
def attachments_embedding_mode(self, value: aspose.words.saving.PdfAttachmentsEmbeddingMode):
    ...

```

### Remarks

Default value is [PdfAttachmentsEmbeddingMode.NONE](../../pdfattachmentsembeddingmode/#NONE) and attachments are not embedded.

PDF/A-1, PDF/A-2 and regular PDF/A-4 (not PDF/A-4f) standards do not allow embedded files.
[PdfAttachmentsEmbeddingMode.NONE](../../pdfattachmentsembeddingmode/#NONE) value will be used automatically.





### Examples

Shows how to add embed attachments to the PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_ole_object(file_name=MY_DIR + 'Spreadsheet.xlsx', prog_id='Excel.Sheet', is_linked=False, as_icon=True, presentation=None)
save_options = aw.saving.PdfSaveOptions()
save_options.attachments_embedding_mode = aw.saving.PdfAttachmentsEmbeddingMode.ANNOTATIONS
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.PdfEmbedAttachments.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

