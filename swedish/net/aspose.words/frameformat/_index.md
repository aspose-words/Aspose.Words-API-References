---
title: FrameFormat Class
linktitle: FrameFormat
articleTitle: FrameFormat
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.FrameFormat för avancerad ramformatering i stycken. Förbättra din dokumentdesign med sömlös integration och flexibilitet.
type: docs
weight: 3500
url: /sv/net/aspose.words/frameformat/
---
## FrameFormat class

Representerar ramrelaterad formatering för ett stycke.

```csharp
public class FrameFormat
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Height](../../aspose.words/frameformat/height/) { get; } | Hämtar höjden på den angivna ramen. |
| [HeightRule](../../aspose.words/frameformat/heightrule/) { get; } | Hämtar regeln för att bestämma höjden på den angivna ramen. |
| [HorizontalAlignment](../../aspose.words/frameformat/horizontalalignment/) { get; } | Hämtar horisontell justering av den angivna ramen. |
| [HorizontalDistanceFromText](../../aspose.words/frameformat/horizontaldistancefromtext/) { get; } | Hämtar det horisontella avståndet mellan en ram och den omgivande texten, i punkter. |
| [HorizontalPosition](../../aspose.words/frameformat/horizontalposition/) { get; } | Hämtar det horisontella avståndet mellan ramens kant och det objekt som anges av[`RelativeHorizontalPosition`](./relativehorizontalposition/) egendom. |
| [IsFrame](../../aspose.words/frameformat/isframe/) { get; } | Returer`sann` om stycket är en ram. |
| [RelativeHorizontalPosition](../../aspose.words/frameformat/relativehorizontalposition/) { get; } | Hämtar den relativa horisontella positionen för en ram. |
| [RelativeVerticalPosition](../../aspose.words/frameformat/relativeverticalposition/) { get; } | Hämtar den relativa vertikala positionen för en ram. |
| [VerticalAlignment](../../aspose.words/frameformat/verticalalignment/) { get; } | Hämtar vertikal justering av den angivna ramen. |
| [VerticalDistanceFromText](../../aspose.words/frameformat/verticaldistancefromtext/) { get; } | Anger vertikalt avstånd (i punkter) mellan en ram och den omgivande texten. |
| [VerticalPosition](../../aspose.words/frameformat/verticalposition/) { get; } | Hämtar det vertikala avståndet mellan ramens kant och det objekt som anges av[`RelativeVerticalPosition`](./relativeverticalposition/) egendom. |
| [Width](../../aspose.words/frameformat/width/) { get; } | Hämtar bredden på den angivna ramen, i punkter. |

## Anmärkningar

Detta objekt skapas alltid. Om ett stycke är en ram kommer alla egenskaper att innehålla respektive värden, annars ställs alla egenskaper in till standardvärdena.

Använda[`IsFrame`](./isframe/)för att kontrollera om stycket är en ram.

## Exempel

Visar hur man får information om formateringsegenskaper för stycken som är ramar.

```csharp
Document doc = new Document(MyDir + "Paragraph frame.docx");

Paragraph paragraphFrame = doc.FirstSection.Body.Paragraphs.OfType<Paragraph>().First(p => p.FrameFormat.IsFrame);

Assert.AreEqual(233.3d, paragraphFrame.FrameFormat.Width);
Assert.AreEqual(138.8d, paragraphFrame.FrameFormat.Height);
Assert.AreEqual(HeightRule.AtLeast, paragraphFrame.FrameFormat.HeightRule);
Assert.AreEqual(HorizontalAlignment.Default, paragraphFrame.FrameFormat.HorizontalAlignment);
Assert.AreEqual(VerticalAlignment.Default, paragraphFrame.FrameFormat.VerticalAlignment);
Assert.AreEqual(34.05d, paragraphFrame.FrameFormat.HorizontalPosition);
Assert.AreEqual(RelativeHorizontalPosition.Page, paragraphFrame.FrameFormat.RelativeHorizontalPosition);
Assert.AreEqual(9.0d, paragraphFrame.FrameFormat.HorizontalDistanceFromText);
Assert.AreEqual(20.5d, paragraphFrame.FrameFormat.VerticalPosition);
Assert.AreEqual(RelativeVerticalPosition.Paragraph, paragraphFrame.FrameFormat.RelativeVerticalPosition);
Assert.AreEqual(0.0d, paragraphFrame.FrameFormat.VerticalDistanceFromText);
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
