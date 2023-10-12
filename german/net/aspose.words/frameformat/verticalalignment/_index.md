---
title: FrameFormat.VerticalAlignment
second_title: Aspose.Words für .NET-API-Referenz
description: FrameFormat eigendom. Ruft die vertikale Ausrichtung des angegebenen Frames ab.
type: docs
weight: 90
url: /de/net/aspose.words/frameformat/verticalalignment/
---
## FrameFormat.VerticalAlignment property

Ruft die vertikale Ausrichtung des angegebenen Frames ab.

```csharp
public VerticalAlignment VerticalAlignment { get; }
```

### Beispiele

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

* enum [VerticalAlignment](../../../aspose.words.drawing/verticalalignment/)
* class [FrameFormat](../)
* namensraum [Aspose.Words](../../frameformat/)
* Montage [Aspose.Words](../../../)


