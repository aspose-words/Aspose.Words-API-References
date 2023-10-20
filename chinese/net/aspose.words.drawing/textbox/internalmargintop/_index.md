---
title: TextBox.InternalMarginTop
linktitle: InternalMarginTop
articleTitle: InternalMarginTop
second_title: 用于 .NET 的 Aspose.Words
description: TextBox InternalMarginTop 财产. 指定形状的内部上边距以磅为单位 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words.drawing/textbox/internalmargintop/
---
## TextBox.InternalMarginTop property

指定形状的内部上边距（以磅为单位）。

```csharp
public double InternalMarginTop { get; set; }
```

## 评论

默认值为 1/20 英寸。

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

### 也可以看看

* class [TextBox](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
