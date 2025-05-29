---
title: TextWatermarkOptions.FontSize
linktitle: FontSize
articleTitle: FontSize
second_title: Aspose.Words för .NET
description: Anpassa dina TextWatermarkOptions med justerbar teckenstorlek. Ställ enkelt in önskad storlek för optimal synlighet och stil i dina designer.
type: docs
weight: 40
url: /sv/net/aspose.words/textwatermarkoptions/fontsize/
---
## TextWatermarkOptions.FontSize property

Hämtar eller ställer in en teckenstorlek. Standardvärdet är 0 - auto.

```csharp
public float FontSize { get; set; }
```

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentOutOfRangeException | Kasta ett värde när argumentet låg utanför intervallet för giltiga värden. |

## Anmärkningar

Giltiga värden sträcker sig från 0 till 65,5.

Automatisk teckenstorlek innebär att vattenstämpeln skalas till sin maximala bredd och maximala höjd i förhållande till sidmarginalerna.

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
