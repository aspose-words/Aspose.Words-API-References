---
title: FrameFormat Class
linktitle: FrameFormat
articleTitle: FrameFormat
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.FrameFormat 类，用于段落中的高级框架格式设置。通过无缝集成和灵活性增强您的文档设计。
type: docs
weight: 3500
url: /zh/net/aspose.words/frameformat/
---
## FrameFormat class

表示段落的框架相关格式。

```csharp
public class FrameFormat
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Height](../../aspose.words/frameformat/height/) { get; } | 获取指定框架的高度。 |
| [HeightRule](../../aspose.words/frameformat/heightrule/) { get; } | 获取确定指定框架高度的规则。 |
| [HorizontalAlignment](../../aspose.words/frameformat/horizontalalignment/) { get; } | 获取指定框架的水平对齐方式。 |
| [HorizontalDistanceFromText](../../aspose.words/frameformat/horizontaldistancefromtext/) { get; } | 获取框架与周围文本之间的水平距离（以点为单位）。 |
| [HorizontalPosition](../../aspose.words/frameformat/horizontalposition/) { get; } | 获取框架边缘与指定项目之间的水平距离[`RelativeHorizontalPosition`](./relativehorizontalposition/)属性. |
| [IsFrame](../../aspose.words/frameformat/isframe/) { get; } | 返回`真的`如果该段落是一个框架。 |
| [RelativeHorizontalPosition](../../aspose.words/frameformat/relativehorizontalposition/) { get; } | 获取框架的相对水平位置。 |
| [RelativeVerticalPosition](../../aspose.words/frameformat/relativeverticalposition/) { get; } | 获取框架的相对垂直位置。 |
| [VerticalAlignment](../../aspose.words/frameformat/verticalalignment/) { get; } | 获取指定框架的垂直对齐方式。 |
| [VerticalDistanceFromText](../../aspose.words/frameformat/verticaldistancefromtext/) { get; } | 指定框架和周围文本之间的垂直距离（以点为单位）。 |
| [VerticalPosition](../../aspose.words/frameformat/verticalposition/) { get; } | 获取框架边缘与指定项目之间的垂直距离[`RelativeVerticalPosition`](./relativeverticalposition/)属性. |
| [Width](../../aspose.words/frameformat/width/) { get; } | 获取指定框架的宽度（以磅为单位）。 |

## 评论

此对象始终会被创建。如果段落是框架，则所有属性都将包含相应的值；否则，所有属性都将设置为默认值。

使用[`IsFrame`](./isframe/)检查段落是否为框架。

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
