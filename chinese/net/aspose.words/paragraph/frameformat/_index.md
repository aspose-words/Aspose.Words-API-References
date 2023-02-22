---
title: Paragraph.FrameFormat
second_title: Aspose.Words for .NET API 参考
description: Paragraph 财产. 提供对段落格式属性的访问
type: docs
weight: 30
url: /zh/net/aspose.words/paragraph/frameformat/
---
## Paragraph.FrameFormat property

提供对段落格式属性的访问。

```csharp
public FrameFormat FrameFormat { get; }
```

### 例子

显示如何获取有关作为框架的段落的格式属性的信息。

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

### 也可以看看

* class [FrameFormat](../../frameformat/)
* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../paragraph/)
* 部件 [Aspose.Words](../../../)


