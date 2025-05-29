---
title: FrameFormat.VerticalAlignment
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: Aspose.Words for .NET
description: 探索 FrameFormat VerticalAlignment 属性，轻松管理框架的垂直对齐，毫不费力地增强布局设计。
type: docs
weight: 90
url: /zh/net/aspose.words/frameformat/verticalalignment/
---
## FrameFormat.VerticalAlignment property

获取指定框架的垂直对齐方式。

```csharp
public VerticalAlignment VerticalAlignment { get; }
```

## 例子

展示如何获取有关框架段落的格式属性的信息。

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

* enum [VerticalAlignment](../../../aspose.words.drawing/verticalalignment/)
* class [FrameFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
