---
title: Aspose::Words::Saving::PdfSaveOptions::set_ExportParagraphGraphicsToArtifact method
linktitle: set_ExportParagraphGraphicsToArtifact
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::set_ExportParagraphGraphicsToArtifact method. Sets a value determining whether a paragraph graphic should be marked as an artifact in C++.'
type: docs
weight: 50500
url: /cpp/aspose.words.saving/pdfsaveoptions/set_exportparagraphgraphicstoartifact/
---
## PdfSaveOptions::set_ExportParagraphGraphicsToArtifact method


Sets a value determining whether a paragraph graphic should be marked as an artifact.

```cpp
void Aspose::Words::Saving::PdfSaveOptions::set_ExportParagraphGraphicsToArtifact(bool value)
```

## Remarks


 Default value is **false** and paragraph graphics (underlines, text emphasis, etc.) will be marked as "Span" in the logical structure of the document.

 When the value is **true** the paragraph graphics will be marked as "Artifact".

 This value is ignored when [ExportDocumentStructure](../get_exportdocumentstructure/) is **false**. 
## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
