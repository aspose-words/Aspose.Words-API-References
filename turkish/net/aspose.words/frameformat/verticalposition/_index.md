---
title: FrameFormat.VerticalPosition
second_title: Aspose.Words for .NET API Referansı
description: FrameFormat mülk. Çerçevenin kenarı ile belirtilen öğe arasındaki dikey mesafeyi alır.RelativeVerticalPosition özellik.
type: docs
weight: 110
url: /tr/net/aspose.words/frameformat/verticalposition/
---
## FrameFormat.VerticalPosition property

Çerçevenin kenarı ile belirtilen öğe arasındaki dikey mesafeyi alır.[`RelativeVerticalPosition`](../relativeverticalposition/) özellik.

```csharp
public double VerticalPosition { get; }
```

### Örnekler

Çerçeve olan paragrafların biçimlendirme özellikleri hakkında nasıl bilgi alınacağını gösterir.

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

### Ayrıca bakınız

* class [FrameFormat](../)
* ad alanı [Aspose.Words](../../frameformat/)
* toplantı [Aspose.Words](../../../)


