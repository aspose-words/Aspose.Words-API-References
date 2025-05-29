---
title: TextBox.InternalMarginRight
linktitle: InternalMarginRight
articleTitle: InternalMarginRight
second_title: Aspose.Words for .NET
description: 探索 TextBox InternalMarginRight 属性，以使用精确的右边距（以点为单位）自定义形状，从而增强设计灵活性。
type: docs
weight: 40
url: /zh/net/aspose.words.drawing/textbox/internalmarginright/
---
## TextBox.InternalMarginRight property

指定形状的内右边距（以磅为单位）。

```csharp
public double InternalMarginRight { get; set; }
```

## 评论

默认值为 1/10 英寸。

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

### 也可以看看

* class [TextBox](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
