---
title: TextWatermarkOptions.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words för .NET
description: Anpassa dina TextWatermarkOptions med egenskapen Color för att förbättra synligheten. Ställ in önskad teckenfärg för en personlig touch. Standard, Silver.
type: docs
weight: 20
url: /sv/net/aspose.words/textwatermarkoptions/color/
---
## TextWatermarkOptions.Color property

Hämtar eller ställer in teckenfärg. Standardvärdet ärSilver .

```csharp
public Color Color { get; set; }
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

* class [TextWatermarkOptions](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
