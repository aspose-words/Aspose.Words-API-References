---
title: Shape.TextBox
linktitle: TextBox
articleTitle: TextBox
second_title: Aspose.Words for .NET
description: 自定义形状文本框属性，增强文本显示效果，提升设计的视觉吸引力。立即释放创意潜能！
type: docs
weight: 230
url: /zh/net/aspose.words.drawing/shape/textbox/
---
## Shape.TextBox property

定义指定文本在形状中显示方式的属性。

```csharp
public TextBox TextBox { get; }
```

## 例子

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

### 也可以看看

* class [TextBox](../../textbox/)
* class [Shape](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
