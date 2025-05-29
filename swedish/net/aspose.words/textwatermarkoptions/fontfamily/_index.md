---
title: TextWatermarkOptions.FontFamily
linktitle: FontFamily
articleTitle: FontFamily
second_title: Aspose.Words för .NET
description: Anpassa dina TextWatermarkOptions med egenskapen FontFamily för att förbättra dina designer. Standardinställningen är Calibri; välj en stil som passar ditt varumärke!
type: docs
weight: 30
url: /sv/net/aspose.words/textwatermarkoptions/fontfamily/
---
## TextWatermarkOptions.FontFamily property

Hämtar eller ställer in teckensnittsfamiljens namn. Standardvärdet är "Calibri".

```csharp
public string FontFamily { get; set; }
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
