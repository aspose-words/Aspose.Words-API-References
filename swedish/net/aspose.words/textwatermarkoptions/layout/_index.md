---
title: TextWatermarkOptions.Layout
linktitle: Layout
articleTitle: Layout
second_title: Aspose.Words för .NET
description: Upptäck layoutegenskapen TextWatermarkOptions för att anpassa ditt vattenstämpels utseende. Ställ enkelt in den på Diagonal eller din föredragna layout för förbättrad grafik.
type: docs
weight: 60
url: /sv/net/aspose.words/textwatermarkoptions/layout/
---
## TextWatermarkOptions.Layout property

Hämtar eller ställer in vattenstämpelns layout. Standardvärdet ärDiagonal .

```csharp
public WatermarkLayout Layout { get; set; }
```

## Exempel

Visar hur man skapar en textvattenstämpel.

```csharp
Document doc = new Document();

// Lägg till ett vattenmärke i vanlig text.
doc.Watermark.SetText("Aspose Watermark");

// Om vi vill redigera textformateringen med hjälp av den som vattenstämpel,
// vi kan göra det genom att skicka ett TextWatermarkOptions-objekt när vi skapar vattenstämpeln.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// Vi kan ta bort en vattenstämpel från ett dokument som detta.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### Se även

* enum [WatermarkLayout](../../watermarklayout/)
* class [TextWatermarkOptions](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
