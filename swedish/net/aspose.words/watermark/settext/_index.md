---
title: Watermark.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words för .NET
description: Förbättra dina dokument med vår metod Watermark SetText. Lägg enkelt till anpassningsbara textvattenmärken för en professionell touch!
type: docs
weight: 40
url: /sv/net/aspose.words/watermark/settext/
---
## SetText(*string*) {#settext}

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
| ArgumentOutOfRangeException | Körs när textlängden är utanför intervallet eller när texten bara innehåller blanksteg. |
| ArgumentNullException | Kasta när texten är`null` . |

## Anmärkningar

Textlängden måste vara inom intervallet 1 till 200. Texten kan inte vara`null` eller innehåller endast mellanslag.

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

* class [Watermark](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## SetText(*string, [TextWatermarkOptions](../../textwatermarkoptions/)*) {#settext_1}

Lägger till textvattenstämpel i dokumentet.

```csharp
public void SetText(string text, TextWatermarkOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| text | String | Text som visas som en vattenstämpel. |
| options | TextWatermarkOptions | Definierar ytterligare alternativ för textvattenmärket. |

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentOutOfRangeException | Körs när textlängden är utanför intervallet eller när texten bara innehåller blanksteg. |
| ArgumentNullException | Kasta när texten är`null` . |

## Anmärkningar

Textlängden måste vara inom intervallet 1 till 200. Texten kan inte vara`null` eller innehåller endast mellanslag.

Om[`TextWatermarkOptions`](../../textwatermarkoptions/) är`null`, kommer vattenstämpeln att ställas in med standardalternativen.

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

* class [TextWatermarkOptions](../../textwatermarkoptions/)
* class [Watermark](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
