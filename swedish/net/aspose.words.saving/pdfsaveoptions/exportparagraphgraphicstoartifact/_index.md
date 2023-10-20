---
title: PdfSaveOptions.ExportParagraphGraphicsToArtifact
linktitle: ExportParagraphGraphicsToArtifact
articleTitle: ExportParagraphGraphicsToArtifact
second_title: Aspose.Words för .NET
description: PdfSaveOptions ExportParagraphGraphicsToArtifact fast egendom. Hämtar eller ställer in ett värde som avgör om en styckegrafik ska markeras som en artefakt i C#.
type: docs
weight: 160
url: /sv/net/aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/
---
## PdfSaveOptions.ExportParagraphGraphicsToArtifact property

Hämtar eller ställer in ett värde som avgör om en styckegrafik ska markeras som en artefakt.

```csharp
public bool ExportParagraphGraphicsToArtifact { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk` och styckegrafik (understrykningar, betoning av text, etc.) kommer att markeras som "Span" i dokumentets logiska struktur.

När värdet är`Sann` styckegrafiken kommer att markeras som "Artefakt".

Detta värde ignoreras när[`ExportDocumentStructure`](../exportdocumentstructure/) är`falsk` .

## Exempel

Visar hur man exporterar styckegrafik som artefakt (understrykningar, betoning av text, etc.).

```csharp
Document doc = new Document(MyDir + "PDF artifacts.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.ExportDocumentStructure = true;
saveOptions.ExportParagraphGraphicsToArtifact = true;
saveOptions.TextCompression = PdfTextCompression.None;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportParagraphGraphicsToArtifact.pdf", saveOptions);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
