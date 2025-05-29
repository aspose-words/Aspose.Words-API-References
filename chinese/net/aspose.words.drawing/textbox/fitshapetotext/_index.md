---
title: TextBox.FitShapeToText
linktitle: FitShapeToText
articleTitle: FitShapeToText
second_title: Aspose.Words for .NET
description: 了解 Microsoft Word 中的 FitShapeToText 属性如何自动调整形状以完美适合您的文本，从而增强文档的呈现效果。
type: docs
weight: 10
url: /zh/net/aspose.words.drawing/textbox/fitshapetotext/
---
## TextBox.FitShapeToText property

确定 Microsoft Word 是否会扩大形状以适应文本。

```csharp
public bool FitShapeToText { get; set; }
```

## 评论

默认值为`错误的`。

## 例子

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

* class [TextBox](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
