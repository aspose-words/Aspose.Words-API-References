---
title: TextBox.InternalMarginBottom
linktitle: InternalMarginBottom
articleTitle: InternalMarginBottom
second_title: 用于 .NET 的 Aspose.Words
description: TextBox InternalMarginBottom 财产. 指定形状的内部底部边距以磅为单位 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.drawing/textbox/internalmarginbottom/
---
## TextBox.InternalMarginBottom property

指定形状的内部底部边距（以磅为单位）。

```csharp
public double InternalMarginBottom { get; set; }
```

## 评论

默认值为 1/20 英寸。

## 例子

演示如何设置文本框的内部边距。

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
