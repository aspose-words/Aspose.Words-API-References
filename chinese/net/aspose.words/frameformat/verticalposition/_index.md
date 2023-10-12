---
title: FrameFormat.VerticalPosition
second_title: Aspose.Words for .NET API 参考
description: FrameFormat 财产. 获取框架边缘与指定项目之间的垂直距离RelativeVerticalPosition属性.
type: docs
weight: 110
url: /zh/net/aspose.words/frameformat/verticalposition/
---
## FrameFormat.VerticalPosition property

获取框架边缘与指定项目之间的垂直距离[`RelativeVerticalPosition`](../relativeverticalposition/)属性.

```csharp
public double VerticalPosition { get; }
```

### 例子

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

* class [FrameFormat](../)
* 命名空间 [Aspose.Words](../../frameformat/)
* 部件 [Aspose.Words](../../../)


