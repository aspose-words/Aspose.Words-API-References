---
title: WatermarkType Enum
linktitle: WatermarkType
articleTitle: WatermarkType
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.WatermarkType-enum för enkel anpassning av vattenstämplar i dokument. Förbättra dina projekt med mångsidiga vattenstämpelalternativ!
type: docs
weight: 7540
url: /sv/net/aspose.words/watermarktype/
---
## WatermarkType enumeration

Anger vattenstämpeltypen.

```csharp
public enum WatermarkType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Text | `0` | Anger att texten kommer att användas som vattenstämpel. |
| Image | `1` | Anger att bilden kommer att användas som vattenstämpel. |
| None | `2` | Indikerar att vattenstämpeln inte är angiven. |

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
