---
title: FrameFormat.RelativeHorizontalPosition
linktitle: RelativeHorizontalPosition
articleTitle: RelativeHorizontalPosition
second_title: .NET için Aspose.Words
description: Gelişmiş düzen kontrolü için bir çerçevenin yatay konumunu kolayca belirlemek amacıyla FrameFormat RelativeHorizontalPosition özelliğini keşfedin.
type: docs
weight: 70
url: /tr/net/aspose.words/frameformat/relativehorizontalposition/
---
## FrameFormat.RelativeHorizontalPosition property

Bir çerçevenin göreceli yatay konumunu alır.

```csharp
public RelativeHorizontalPosition RelativeHorizontalPosition { get; }
```

## Örnekler

Çerçeve olan paragrafların biçimlendirme özellikleri hakkında bilgi edinmenin nasıl yapılacağını gösterir.

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

* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* class [FrameFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
