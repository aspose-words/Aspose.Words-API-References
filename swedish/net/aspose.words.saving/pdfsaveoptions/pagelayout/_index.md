---
title: PdfSaveOptions.PageLayout
linktitle: PageLayout
articleTitle: PageLayout
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PdfSaveOptions PageLayout för att anpassa din PDF-fils layout för optimal visning i alla läsare. Förbättra dokumentets presentation!
type: docs
weight: 250
url: /sv/net/aspose.words.saving/pdfsaveoptions/pagelayout/
---
## PdfSaveOptions.PageLayout property

Anger vilken sidlayout som ska användas när dokumentet öppnas i en PDF-läsare.

```csharp
public PdfPageLayout PageLayout { get; set; }
```

## Anmärkningar

Standardvärdet ärSinglePage .

## Exempel

Visar hur sidor visas när de öppnas i en PDF-läsare.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Visa sidorna två åt gången, med udda sidor till vänster.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PageLayout = PdfPageLayout.TwoPageLeft;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageLayout.pdf", saveOptions);
```

### Se även

* enum [PdfPageLayout](../../pdfpagelayout/)
* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
