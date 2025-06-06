---
title: TextBox Class
linktitle: TextBox
articleTitle: TextBox
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.TextBox 类，轻松自定义形状内的文本显示，增强文档的视觉吸引力和功能。
type: docs
weight: 1730
url: /zh/net/aspose.words.drawing/textbox/
---
## TextBox class

定义指定文本在形状内如何显示的属性。

要了解更多信息，请访问[使用形状](https://docs.aspose.com/words/net/working-with-shapes/)文档文章。

```csharp
public class TextBox
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [FitShapeToText](../../aspose.words.drawing/textbox/fitshapetotext/) { get; set; } | 确定 Microsoft Word 是否会扩大形状以适应文本。 |
| [InternalMarginBottom](../../aspose.words.drawing/textbox/internalmarginbottom/) { get; set; } | 指定形状的内底边距（以点为单位）。 |
| [InternalMarginLeft](../../aspose.words.drawing/textbox/internalmarginleft/) { get; set; } | 指定形状的左边距（以磅为单位）。 |
| [InternalMarginRight](../../aspose.words.drawing/textbox/internalmarginright/) { get; set; } | 指定形状的内右边距（以磅为单位）。 |
| [InternalMarginTop](../../aspose.words.drawing/textbox/internalmargintop/) { get; set; } | 指定形状的内部上边距（以点为单位）。 |
| [LayoutFlow](../../aspose.words.drawing/textbox/layoutflow/) { get; set; } | 确定形状中文本布局的流程。 |
| [Next](../../aspose.words.drawing/textbox/next/) { get; set; } | 返回或设置`TextBox`代表下一个`TextBox`按照形状序列排列。 |
| [NoTextRotation](../../aspose.words.drawing/textbox/notextrotation/) { get; set; } | 获取或设置一个布尔值，指示当形状旋转时，TextBox 的文本不应旋转。 |
| [Parent](../../aspose.words.drawing/textbox/parent/) { get; } | 获取父形状`TextBox`. |
| [Previous](../../aspose.words.drawing/textbox/previous/) { get; } | 返回`TextBox`代表前一个`TextBox`按照形状序列排列。 |
| [TextBoxWrapMode](../../aspose.words.drawing/textbox/textboxwrapmode/) { get; set; } | 确定文本在形状内如何换行。 |
| [VerticalAnchor](../../aspose.words.drawing/textbox/verticalanchor/) { get; set; } | 指定形状内文本的垂直对齐方式。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [BreakForwardLink](../../aspose.words.drawing/textbox/breakforwardlink/)() | 断开到下一个的链接`TextBox`. |
| [IsValidLinkTarget](../../aspose.words.drawing/textbox/isvalidlinktarget/)(*TextBox*) | 确定这`TextBox`可以链接到目标`TextBox`. |

## 评论

使用[`TextBox`](../shape/textbox/)属性来访问形状的文本属性。 您不创建`TextBox`直接上课。

## 例子

展示如何设置文本框的内部边距。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入另一个具有特定边距的文本框。
Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox = textBoxShape.TextBox;
textBox.InternalMarginTop = 15;
textBox.InternalMarginBottom = 15;
textBox.InternalMarginLeft = 15;
textBox.InternalMarginRight = 15;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text placed according to textbox margins.");

doc.Save(ArtifactsDir + "Shape.TextBoxMargins.docx");
```

展示如何设置文本框内文本的方向。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// 将文档构建器移动到文本框内并添加文本。
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// 设置“LayoutFlow”属性来设置此文本框的文本内容的方向。
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

展示如何让文本框调整自身大小以紧密适应其内容。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// 将这些值应用于这两个成员以使父形状适合
// 紧紧围绕文本内容，忽略我们设置的尺寸。
textBox.FitShapeToText = true;
textBox.TextBoxWrapMode = TextBoxWrapMode.None;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text fit tightly inside textbox.");

doc.Save(ArtifactsDir + "Shape.TextBoxFitShapeToText.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
