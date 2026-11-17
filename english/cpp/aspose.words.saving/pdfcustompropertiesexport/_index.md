---
title: Aspose::Words::Saving::PdfCustomPropertiesExport enum
linktitle: PdfCustomPropertiesExport
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfCustomPropertiesExport enum. Specifies the way CustomDocumentProperties are exported to PDF file in C++.'
type: docs
weight: 74000
url: /cpp/aspose.words.saving/pdfcustompropertiesexport/
---
## PdfCustomPropertiesExport enum


Specifies the way [CustomDocumentProperties](../../aspose.words/document/get_customdocumentproperties/) are exported to PDF file.

```cpp
enum class PdfCustomPropertiesExport
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | No custom properties are exported. |
| Standard | 1 | Custom properties are exported as entries in /Info dictionary. Custom properties with the following names are not exported: "Title", "Author", "Subject", "Keywords", "Creator", "Producer", "CreationDate", "ModDate", "Trapped". |
| Metadata | 2 | Custom properties are Metadata. |

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
