---
title: Watermark.SetText
second_title: Aspose.Words för .NET API Referens
description: Watermark metod. Lägger till textvattenstämpel i dokumentet.
type: docs
weight: 40
url: /sv/net/aspose.words/watermark/settext/
---
## SetText(string) {#settext}

Lägger till textvattenstämpel i dokumentet.

```csharp
public void SetText(string text)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| text | String | Text som visas som en vattenstämpel. |

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentOutOfRangeException | Kastar när textlängden är utanför intervallet eller texten endast innehåller blanksteg. |
| ArgumentNullException | Kastar när texten är`null` . |

### Anmärkningar

Textlängden måste vara i intervallet från 1 till 200 inklusive. Texten kan inte vara`null` eller bara innehålla blanksteg.

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

---

## SetText(string, TextWatermarkOptions) {#settext_1}

Lägger till textvattenstämpel i dokumentet.

```csharp
public void SetText(string text, TextWatermarkOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| text | String | Text som visas som en vattenstämpel. |
| options | TextWatermarkOptions | Definierar ytterligare alternativ för textens vattenstämpel. |

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentOutOfRangeException | Kastar när textlängden är utanför intervallet eller texten bara innehåller blanksteg. |
| ArgumentNullException | Kastar när texten är`null` . |

### Anmärkningar

Textlängden måste vara i intervallet från 1 till 200 inklusive. Texten kan inte vara`null` eller bara innehålla blanksteg.

Om[`TextWatermarkOptions`](../../textwatermarkoptions/) är`null`, kommer vattenstämpeln att ställas in med standardalternativ.

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

* class [TextWatermarkOptions](../../textwatermarkoptions/)
* class [Watermark](../)
* namnutrymme [Aspose.Words](../../watermark/)
* hopsättning [Aspose.Words](../../../)


