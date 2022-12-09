---
title: get_EmbedAttachments
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value determining whether or not to embed attachments to the PDF document.
type: docs
weight: 157
url: /cpp/aspose.words.saving/pdfsaveoptions/get_embedattachments/
---
## PdfSaveOptions::get_EmbedAttachments method


Gets or sets a value determining whether or not to embed attachments to the PDF document.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_EmbedAttachments() const
```

## Remarks


Default value is **false** and attachments are not embedded.

When the value is **true** attachments are embedded to the PDF document.

Embedding attachments is not supported when saving to PDF/A and PDF/UA compliance. **false** value will be used automatically.

Embedding attachments is not supported when encryption is enabled. **false** value will be used automatically. 
## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
