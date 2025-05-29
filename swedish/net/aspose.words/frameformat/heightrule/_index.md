---
title: FrameFormat.HeightRule
linktitle: HeightRule
articleTitle: HeightRule
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FrameFormat HeightRule för att enkelt bestämma ramhöjden. Optimera dina designer med exakt kontroll och förbättrad layouteffektivitet.
type: docs
weight: 20
url: /sv/net/aspose.words/frameformat/heightrule/
---
## FrameFormat.HeightRule property

Hämtar regeln för att bestämma höjden på den angivna ramen.

```csharp
public HeightRule HeightRule { get; }
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

* enum [HeightRule](../../heightrule/)
* class [FrameFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
