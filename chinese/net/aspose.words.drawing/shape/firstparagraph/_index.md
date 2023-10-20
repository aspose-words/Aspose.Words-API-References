---
title: Shape.FirstParagraph
linktitle: FirstParagraph
articleTitle: FirstParagraph
second_title: 用于 .NET 的 Aspose.Words
description: Shape FirstParagraph 财产. 获取形状中的第一段 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words.drawing/shape/firstparagraph/
---
## Shape.FirstParagraph property

获取形状中的第一段。

```csharp
public Paragraph FirstParagraph { get; }
```

## 例子

演示如何创建文本框并设置其格式。

```csharp
Document doc = new Document();

// 创建一个浮动文本框。
Shape textBox = new Shape(doc, ShapeType.TextBox);
textBox.WrapType = WrapType.None;
textBox.Height = 50;
textBox.Width = 200;

// 设置形状内文本的水平和垂直对齐方式。
textBox.HorizontalAlignment = HorizontalAlignment.Center;
textBox.VerticalAlignment = VerticalAlignment.Top;

// 将一个段落添加到文本框并添加文本框将显示的一系列文本。
textBox.AppendChild(new Paragraph(doc));
Paragraph para = textBox.FirstParagraph;
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;
Run run = new Run(doc);
run.Text = "Hello world!";
para.AppendChild(run);

doc.FirstSection.Body.FirstParagraph.AppendChild(textBox);

doc.Save(ArtifactsDir + "Shape.CreateTextBox.docx");
```

### 也可以看看

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Shape](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
