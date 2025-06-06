---
title: FrameFormat.HeightRule
linktitle: HeightRule
articleTitle: HeightRule
second_title: .NET için Aspose.Words
description: Çerçeve yüksekliğini kolayca belirlemek için FrameFormat HeightRule özelliğini keşfedin. Tasarımlarınızı hassas kontrol ve iyileştirilmiş düzen verimliliğiyle optimize edin.
type: docs
weight: 20
url: /tr/net/aspose.words/frameformat/heightrule/
---
## FrameFormat.HeightRule property

Belirtilen çerçevenin yüksekliğini belirleme kuralını alır.

```csharp
public HeightRule HeightRule { get; }
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

* enum [HeightRule](../../heightrule/)
* class [FrameFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
