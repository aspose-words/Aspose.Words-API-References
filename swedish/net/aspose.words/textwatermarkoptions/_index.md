---
title: TextWatermarkOptions Class
linktitle: TextWatermarkOptions
articleTitle: TextWatermarkOptions
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.TextWatermarkOptions för anpassningsbara textvattenmärken. Förbättra dina dokument med unika, professionella varumärkesalternativ!
type: docs
weight: 7290
url: /sv/net/aspose.words/textwatermarkoptions/
---
## TextWatermarkOptions class

Innehåller alternativ som kan anges när man lägger till en vattenstämpel med text.

För att lära dig mer, besök[Arbeta med vattenstämpel](https://docs.aspose.com/words/net/working-with-watermark/) dokumentationsartikel.

```csharp
public class TextWatermarkOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [TextWatermarkOptions](textwatermarkoptions/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Color](../../aspose.words/textwatermarkoptions/color/) { get; set; } | Hämtar eller ställer in teckenfärg. Standardvärdet ärSilver . |
| [FontFamily](../../aspose.words/textwatermarkoptions/fontfamily/) { get; set; } | Hämtar eller ställer in teckensnittsfamiljens namn. Standardvärdet är "Calibri". |
| [FontSize](../../aspose.words/textwatermarkoptions/fontsize/) { get; set; } | Hämtar eller ställer in en teckenstorlek. Standardvärdet är 0 - auto. |
| [IsSemitrasparent](../../aspose.words/textwatermarkoptions/issemitrasparent/) { get; set; } | Hämtar eller ställer in ett booleskt värde som ansvarar för vattenstämpelns opacitet. Standardvärdet är`sann` . |
| [Layout](../../aspose.words/textwatermarkoptions/layout/) { get; set; } | Hämtar eller ställer in vattenstämpelns layout. Standardvärdet ärDiagonal . |

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

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
