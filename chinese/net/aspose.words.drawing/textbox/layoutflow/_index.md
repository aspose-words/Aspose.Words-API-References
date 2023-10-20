---
title: TextBox.LayoutFlow
linktitle: LayoutFlow
articleTitle: LayoutFlow
second_title: 用于 .NET 的 Aspose.Words
description: TextBox LayoutFlow 财产. 确定形状中文本布局的流程 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words.drawing/textbox/layoutflow/
---
## TextBox.LayoutFlow property

确定形状中文本布局的流程。

```csharp
public LayoutFlow LayoutFlow { get; set; }
```

## 评论

默认值为Horizontal。

## 例子

演示如何设置文本框中文本的方向。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// 将文档生成器移动到文本框内部并添加文本。
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// 设置“LayoutFlow”属性来设置此文本框的文本内容的方向。
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

### 也可以看看

* enum [LayoutFlow](../../layoutflow/)
* class [TextBox](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
