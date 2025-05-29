---
title: Watermark.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Vattenstämpeltyp för att förbättra din design med anpassningsbara vattenstämplar för varumärkesbyggande och skydd. Förhöj din visuella effekt idag!
type: docs
weight: 10
url: /sv/net/aspose.words/watermark/type/
---
## Watermark.Type property

Hämtar vattenmärkestypen.

```csharp
public WatermarkType Type { get; }
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

* enum [WatermarkType](../../watermarktype/)
* class [Watermark](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
