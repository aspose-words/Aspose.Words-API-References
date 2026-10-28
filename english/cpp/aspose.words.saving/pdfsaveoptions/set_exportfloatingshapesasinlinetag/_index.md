---
title: Aspose::Words::Saving::PdfSaveOptions::set_ExportFloatingShapesAsInlineTag method
linktitle: set_ExportFloatingShapesAsInlineTag
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::set_ExportFloatingShapesAsInlineTag method. Sets a value determining whether floating shapes are exported as inline tags in the document structure in C++.'
type: docs
weight: 49500
url: /cpp/aspose.words.saving/pdfsaveoptions/set_exportfloatingshapesasinlinetag/
---
## PdfSaveOptions::set_ExportFloatingShapesAsInlineTag method


Sets a value determining whether floating shapes are exported as inline tags in the document structure.

```cpp
void Aspose::Words::Saving::PdfSaveOptions::set_ExportFloatingShapesAsInlineTag(bool value)
```

## Remarks


 Default value is **false** and floating shapes will be exported as block-level tags, placed after the paragraph in which they are anchored.

 When the value is **true** floating shapes will be exported as inline tags, placed within the paragraph where they are anchored.

 This value is ignored when [ExportDocumentStructure](../get_exportdocumentstructure/) is **false**. 
## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
