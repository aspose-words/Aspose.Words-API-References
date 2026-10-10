---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact metod"
linktitle: "get_ExportParagraphGraphicsToArtifact"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact metod. Hämtar eller anger ett värde som bestämmer om en stycke‑grafik ska markeras som ett artefakt i C++."
type: docs
weight: 17500
url: /sv/cpp/aspose.words.saving/pdfsaveoptions/get_exportparagraphgraphicstoartifact/
---
## PdfSaveOptions::get_ExportParagraphGraphicsToArtifact method


Hämtar eller anger ett värde som bestämmer om en stycke-grafik ska markeras som ett artefakt.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact() const
```

## Anmärkningar


Standardvärdet är **false** och stycke‑grafik (understreck, textbetoning osv.) kommer att markeras som \"Span\" i dokumentets logiska struktur.

När värdet är **true** kommer stycke‑grafiken att markeras som \"Artifact\".

Detta värde ignoreras när [ExportDocumentStructure](../get_exportdocumentstructure/) är **false**.
## Se även

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
