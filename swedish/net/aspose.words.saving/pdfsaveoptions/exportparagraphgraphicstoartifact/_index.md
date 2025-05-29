---
title: PdfSaveOptions.ExportParagraphGraphicsToArtifact
linktitle: ExportParagraphGraphicsToArtifact
articleTitle: ExportParagraphGraphicsToArtifact
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PdfSaveOptions ExportParagraphGraphicsToArtifact för att styra styckegrafik som artefakter, vilket förbättrar dokumentets visuella tydlighet.
type: docs
weight: 160
url: /sv/net/aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/
---
## PdfSaveOptions.ExportParagraphGraphicsToArtifact property

Hämtar eller anger ett värde som avgör om en styckegrafik ska markeras som en artefakt.

```csharp
public bool ExportParagraphGraphicsToArtifact { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk` och styckegrafik (understrykningar, textbetoning etc.) kommer att markeras som "Spännvidd" i dokumentets logiska struktur.

När värdet är`sann` Styckegrafiken kommer att markeras som "Artefakt".

Detta värde ignoreras när[`ExportDocumentStructure`](../exportdocumentstructure/) är`falsk` .

## Exempel

Visar hur man exporterar styckegrafik som artefakt (understrykningar, textbetoning etc.).

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
