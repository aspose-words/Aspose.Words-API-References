---
title: FrameFormat.VerticalPosition
second_title: Aspose.Words per .NET API Reference
description: FrameFormat proprietà. Ottiene la distanza verticale tra il bordo della cornice e lelemento specificato daRelativeVerticalPosition proprietà.
type: docs
weight: 110
url: /it/net/aspose.words/frameformat/verticalposition/
---
## FrameFormat.VerticalPosition property

Ottiene la distanza verticale tra il bordo della cornice e l'elemento specificato da[`RelativeVerticalPosition`](../relativeverticalposition/) proprietà.

```csharp
public double VerticalPosition { get; }
```

### Esempi

Mostra come ottenere informazioni sulle proprietà di formattazione dei paragrafi che sono frame.

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

### Guarda anche

* class [FrameFormat](../)
* spazio dei nomi [Aspose.Words](../../frameformat/)
* assemblea [Aspose.Words](../../../)


