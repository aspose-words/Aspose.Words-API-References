---
title: FrameFormat.HorizontalPosition
linktitle: HorizontalPosition
articleTitle: HorizontalPosition
second_title: Aspose.Words für .NET
description: FrameFormat HorizontalPosition eigendom. Ruft den horizontalen Abstand zwischen der Kante des Rahmens und dem durch das angegebenen Element abRelativeHorizontalPosition Eigenschaft in C#.
type: docs
weight: 50
url: /de/net/aspose.words/frameformat/horizontalposition/
---
## FrameFormat.HorizontalPosition property

Ruft den horizontalen Abstand zwischen der Kante des Rahmens und dem durch das angegebenen Element ab[`RelativeHorizontalPosition`](../relativehorizontalposition/) Eigenschaft.

```csharp
public double HorizontalPosition { get; }
```

## Beispiele

Zeigt, wie Sie Informationen zu Formatierungseigenschaften von Absätzen erhalten, die Rahmen sind.

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

### Siehe auch

* class [FrameFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
