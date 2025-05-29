---
title: Watermark Class
linktitle: Watermark
articleTitle: Watermark
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Watermark för att enkelt lägga till och anpassa vattenstämplar i dina dokument, vilket förbättrar professionalism och varumärkesbyggande.
type: docs
weight: 7520
url: /sv/net/aspose.words/watermark/
---
## Watermark class

Representerar klassen som ska arbeta med dokumentets vattenstämpel.

För att lära dig mer, besök[Arbeta med vattenstämpel](https://docs.aspose.com/words/net/working-with-watermark/) dokumentationsartikel.

```csharp
public sealed class Watermark
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Type](../../aspose.words/watermark/type/) { get; } | Hämtar vattenmärkestypen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Remove](../../aspose.words/watermark/remove/)() | Tar bort vattenstämpeln. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage)(*Image*) | Lägger till bildvattenstämpel i dokumentet. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_1)(*Image, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Lägger till bildvattenstämpel i dokumentet. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_2)(*Stream, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Lägger till bildvattenstämpel i dokumentet. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_3)(*string, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Lägger till bildvattenstämpel i dokumentet. |
| [SetText](../../aspose.words/watermark/settext/#settext)(*string*) | Lägger till textvattenstämpel i dokumentet. |
| [SetText](../../aspose.words/watermark/settext/#settext_1)(*string, [TextWatermarkOptions](../textwatermarkoptions/)*) | Lägger till textvattenstämpel i dokumentet. |

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
