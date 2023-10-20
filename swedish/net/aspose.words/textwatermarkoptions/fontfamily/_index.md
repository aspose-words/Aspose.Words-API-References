---
title: TextWatermarkOptions.FontFamily
linktitle: FontFamily
articleTitle: FontFamily
second_title: Aspose.Words för .NET
description: TextWatermarkOptions FontFamily fast egendom. Hämtar eller ställer in teckensnittets efternamn. Standardvärdet är Calibri i C#.
type: docs
weight: 30
url: /sv/net/aspose.words/textwatermarkoptions/fontfamily/
---
## TextWatermarkOptions.FontFamily property

Hämtar eller ställer in teckensnittets efternamn. Standardvärdet är "Calibri".

```csharp
public string FontFamily { get; set; }
```

## Exempel

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
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
