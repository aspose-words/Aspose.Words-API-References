---
title: FrameFormat.VerticalPosition
second_title: Aspose.Words für .NET-API-Referenz
description: FrameFormat eigendom. Ruft den vertikalen Abstand zwischen dem Rand des Rahmens und dem durch den angegebenen Gegenstand abRelativeVerticalPosition Eigentum.
type: docs
weight: 110
url: /de/net/aspose.words/frameformat/verticalposition/
---
## FrameFormat.VerticalPosition property

Ruft den vertikalen Abstand zwischen dem Rand des Rahmens und dem durch den angegebenen Gegenstand ab[`RelativeVerticalPosition`](../relativeverticalposition/) Eigentum.

```csharp
public double VerticalPosition { get; }
```

### Beispiele

Zeigt, wie Informationen zu Formatierungseigenschaften von Absätzen abgerufen werden, die Rahmen sind.

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
* namensraum [Aspose.Words](../../frameformat/)
* Montage [Aspose.Words](../../../)


