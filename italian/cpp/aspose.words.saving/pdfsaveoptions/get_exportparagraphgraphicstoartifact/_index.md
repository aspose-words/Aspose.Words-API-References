---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact metodo"
linktitle: "get_ExportParagraphGraphicsToArtifact"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact metodo. Ottiene o imposta un valore che determina se un elemento grafico del paragrafo deve essere contrassegnato come artefatto in C++."
type: docs
weight: 17500
url: /it/cpp/aspose.words.saving/pdfsaveoptions/get_exportparagraphgraphicstoartifact/
---
## PdfSaveOptions::get_ExportParagraphGraphicsToArtifact method


Ottiene o imposta un valore che determina se un elemento grafico di un paragrafo deve essere contrassegnato come artefatto.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact() const
```

## Note


Il valore predefinito è **false** e le grafiche dei paragrafi (sottolineature, enfasi del testo, ecc.) saranno contrassegnate come "Span" nella struttura logica del documento.

Quando il valore è **true** le grafiche dei paragrafi saranno contrassegnate come "Artifact".

Questo valore è ignorato quando [ExportDocumentStructure](../get_exportdocumentstructure/) è **false**.
## Vedi anche

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
