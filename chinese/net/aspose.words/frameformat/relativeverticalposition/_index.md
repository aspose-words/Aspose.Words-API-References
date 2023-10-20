---
title: FrameFormat.RelativeVerticalPosition
linktitle: RelativeVerticalPosition
articleTitle: RelativeVerticalPosition
second_title: 用于 .NET 的 Aspose.Words
description: FrameFormat RelativeVerticalPosition 财产. 获取帧的相对垂直位置 在 C#.
type: docs
weight: 80
url: /zh/net/aspose.words/frameformat/relativeverticalposition/
---
## FrameFormat.RelativeVerticalPosition property

获取帧的相对垂直位置。

```csharp
public RelativeVerticalPosition RelativeVerticalPosition { get; }
```

## 例子

演示如何获取有关框架段落的格式设置属性的信息。

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

* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* class [FrameFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
