---
title: PdfSaveOptions.embed_attachments property
linktitle: embed_attachments property
articleTitle: embed_attachments property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.embed_attachments property. Gets or sets a value determining whether or not to embed attachments to the PDF document."
type: docs
weight: 110
url: /python-net/aspose.words.saving/pdfsaveoptions/embed_attachments/
---

## PdfSaveOptions.embed_attachments property

Gets or sets a value determining whether or not to embed attachments to the PDF document.


```python
@property
def embed_attachments(self) -> bool:
    ...

@embed_attachments.setter
def embed_attachments(self, value: bool):
    ...

```

### Remarks

Default value is ``False`` and attachments are not embedded.

When the value is ``True`` attachments are embedded to the PDF document.

Embedding attachments is not supported when saving to PDF/A and PDF/UA compliance.
``False`` value will be used automatically.

Embedding attachments is not supported when encryption is enabled. ``False`` value
will be used automatically.




### Examples

Shows how to add embed attachments to the PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc);

builder.insert_ole_object(MY_DIR + "Spreadsheet.xlsx", "Excel.Sheet", False, True, None)

options = aw.saving.PdfSaveOptions()
options.embed_attachments = True

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.PdfEmbedAttachments.pdf", options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

