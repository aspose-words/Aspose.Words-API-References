---
title: FrameFormat.HorizontalAlignment
linktitle: HorizontalAlignment
articleTitle: HorizontalAlignment
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FrameFormat HorizontalAlignment för att enkelt justera och optimera din rams horisontella justering för bättre designkontroll.
type: docs
weight: 30
url: /sv/net/aspose.words/frameformat/horizontalalignment/
---
## FrameFormat.HorizontalAlignment property

Hämtar horisontell justering av den angivna ramen.

```csharp
public HorizontalAlignment HorizontalAlignment { get; }
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

* enum [HorizontalAlignment](../../../aspose.words.drawing/horizontalalignment/)
* class [FrameFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
