---
title: Watermark.Remove
second_title: Aspose.Words för .NET API Referens
description: Watermark metod. Tar bort vattenstämpeln.
type: docs
weight: 20
url: /sv/net/aspose.words/watermark/remove/
---
## Watermark.Remove method

Tar bort vattenstämpeln.

```csharp
public void Remove()
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

* class [Watermark](../)
* namnutrymme [Aspose.Words](../../watermark/)
* hopsättning [Aspose.Words](../../../)


