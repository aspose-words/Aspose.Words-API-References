---
title: PdfSaveOptions.embed_attachments property
linktitle: embed_attachments property
articleTitle: embed_attachments property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.embed_attachments property. Gets or sets a value determining whether or not to embed attachments to the PDF document."
type: docs
weight: 120
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

PDF/A-1, PDF/A-2 and PDF/A-4 (not level F) standards do not allow embedded files.
``False`` value will be used automatically.


Embedding attachments is not supported when encryption is enabled. ``False`` value
will be used automatically.




### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

