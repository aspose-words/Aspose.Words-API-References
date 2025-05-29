---
title: FrameFormat.VerticalPosition
linktitle: VerticalPosition
articleTitle: VerticalPosition
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FrameFormat VerticalPosition, som mäter det vertikala avståndet från ramkanten till ditt angivna objekt, vilket förbättrar layoutprecisionen.
type: docs
weight: 110
url: /sv/net/aspose.words/frameformat/verticalposition/
---
## FrameFormat.VerticalPosition property

Hämtar det vertikala avståndet mellan ramens kant och det objekt som anges av[`RelativeVerticalPosition`](../relativeverticalposition/) egendom.

```csharp
public double VerticalPosition { get; }
```

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

* class [FrameFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
