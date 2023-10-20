---
title: TextBox Class
linktitle: TextBox
articleTitle: TextBox
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.TextBox 班级. 定义指定文本如何在形状内显示的属性 在 C#.
type: docs
weight: 1320
url: /zh/net/aspose.words.drawing/textbox/
---
## TextBox class

定义指定文本如何在形状内显示的属性。

```csharp
public class TextBox
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [FitShapeToText](../../aspose.words.drawing/textbox/fitshapetotext/) { get; set; } | 确定 Microsoft Word 是否会增大形状以适合文本。 |
| [InternalMarginBottom](../../aspose.words.drawing/textbox/internalmarginbottom/) { get; set; } | 以磅为单位指定形状的内底边距。 |
| [InternalMarginLeft](../../aspose.words.drawing/textbox/internalmarginleft/) { get; set; } | 以点为单位指定形状的内部左边距。 |
| [InternalMarginRight](../../aspose.words.drawing/textbox/internalmarginright/) { get; set; } | 以磅为单位指定形状的内右边距。 |
| [InternalMarginTop](../../aspose.words.drawing/textbox/internalmargintop/) { get; set; } | 指定形状的内部上边距（以磅为单位）。 |
| [LayoutFlow](../../aspose.words.drawing/textbox/layoutflow/) { get; set; } | 确定形状中文本布局的流向。 |
| [Next](../../aspose.words.drawing/textbox/next/) { get; set; } | 返回或设置一个文本框，它表示形状序列中的下一个文本框。 |
| [NoTextRotation](../../aspose.words.drawing/textbox/notextrotation/) { get; set; } |  |
| [Parent](../../aspose.words.drawing/textbox/parent/) { get; } | 获取 TextBox 的父形状。 |
| [Previous](../../aspose.words.drawing/textbox/previous/) { get; } | 返回一个文本框，它表示形状序列中的前一个文本框。 |
| [TextBoxWrapMode](../../aspose.words.drawing/textbox/textboxwrapmode/) { get; set; } | 确定文本在形状内的换行方式。 |
| [VerticalAnchor](../../aspose.words.drawing/textbox/verticalanchor/) { get; set; } | 指定形状内文本的垂直对齐方式。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [BreakForwardLink](../../aspose.words.drawing/textbox/breakforwardlink/)() | 断开到下一个文本框的链接。 |
| [IsValidLinkTarget](../../aspose.words.drawing/textbox/isvalidlinktarget/)(*TextBox*) | 判断这个TextBox是否可以链接到目标Textbox。 |

## 评论

使用[`TextBox`](../shape/textbox/)属性来访问形状的文本属性。 您不创建`TextBox`直接上课。

## 例子

显示如何设置文本框的内部边距。

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

演示如何设置文本框内的文本方向。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// 将文档构建器移动到 TextBox 内部并添加文本。
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// 设置“LayoutFlow”属性以设置此文本框文本内容的方向。
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

演示如何让文本框调整自身大小以紧密适应其内容。

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
