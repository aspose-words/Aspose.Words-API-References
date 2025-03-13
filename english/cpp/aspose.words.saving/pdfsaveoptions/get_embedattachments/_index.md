---
title: Aspose::Words::Saving::PdfSaveOptions::get_EmbedAttachments method
linktitle: get_EmbedAttachments
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::get_EmbedAttachments method. Gets or sets a value determining whether or not to embed attachments to the PDF document in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words.saving/pdfsaveoptions/get_embedattachments/
---
## PdfSaveOptions::get_EmbedAttachments method


Gets or sets a value determining whether or not to embed attachments to the PDF document.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_EmbedAttachments()
```

## Remarks


Default value is **false** and attachments are not embedded.

When the value is **true** attachments are embedded to the PDF document.

PDF/A-1, PDF/A-2 and PDF/A-4 (not level F) standards do not allow embedded files. **false** value will be used automatically.

Embedding attachments is not supported when encryption is enabled. **false** value will be used automatically. 
## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
