---
title: FrameFormat.IsFrame
linktitle: IsFrame
articleTitle: IsFrame
second_title: .NET için Aspose.Words
description: FrameFormat IsFrame özelliğini keşfedin. Paragrafınızın bir çerçeve olup olmadığını kolayca belirleyerek belgenizin düzenini ve tasarımını geliştirin.
type: docs
weight: 60
url: /tr/net/aspose.words/frameformat/isframe/
---
## FrameFormat.IsFrame property

Geri Döndürür`doğru` eğer paragraf bir çerçeve ise.

```csharp
public bool IsFrame { get; }
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

* class [FrameFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
