---
title: Aspose::Words::Saving::PdfSaveOptions::set_ExportLanguageToSpanTag method
linktitle: set_ExportLanguageToSpanTag
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::set_ExportLanguageToSpanTag method. Sets a value determining whether or not to create a "Span" tag in the document structure to export the text language in C++.'
type: docs
weight: 50000
url: /cpp/aspose.words.saving/pdfsaveoptions/set_exportlanguagetospantag/
---
## PdfSaveOptions::set_ExportLanguageToSpanTag method


Sets a value determining whether or not to create a "Span" tag in the document structure to export the text language.

```cpp
void Aspose::Words::Saving::PdfSaveOptions::set_ExportLanguageToSpanTag(bool value)
```

## Remarks


 Default value is **false** and "Lang" attribute is attached to a marked-content sequence in a page content stream.

 When the value is **true** "Span" tag is created for the text with non-default language and "Lang" attribute is attached to this tag.

 This value is ignored when [ExportDocumentStructure](../get_exportdocumentstructure/) is **false**. 
## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
