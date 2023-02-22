---
title: TextWatermarkOptions.IsSemitrasparent
second_title: Aspose.Words för .NET API Referens
description: TextWatermarkOptions fast egendom. Hämtar eller ställer in ett booleskt värde som är ansvarigt för opaciteten för vattenstämpeln. Standardvärdet är True.
type: docs
weight: 50
url: /sv/net/aspose.words/textwatermarkoptions/issemitrasparent/
---
## TextWatermarkOptions.IsSemitrasparent property

Hämtar eller ställer in ett booleskt värde som är ansvarigt för opaciteten för vattenstämpeln. Standardvärdet är True.

```csharp
public bool IsSemitrasparent { get; set; }
```

### Exempel

Visar hur man skapar en textvattenstämpel.

```csharp
Document doc = new Document();

// Lägg till en vanlig text vattenstämpel.
doc.Watermark.SetText("Aspose Watermark");

// Om vi vill redigera textformateringen med den som vattenstämpel,
// vi kan göra det genom att skicka ett TextWatermarkOptions-objekt när du skapar vattenstämpeln.
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

* class [TextWatermarkOptions](../)
* namnutrymme [Aspose.Words](../../textwatermarkoptions/)
* hopsättning [Aspose.Words](../../../)


