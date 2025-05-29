---
title: Shape.FirstParagraph
linktitle: FirstParagraph
articleTitle: FirstParagraph
second_title: Aspose.Words for .NET
description: 轻松检索形状的第一段。使用我们简单易用的“形状第一段”功能，优化文档布局。
type: docs
weight: 70
url: /zh/net/aspose.words.drawing/shape/firstparagraph/
---
## Shape.FirstParagraph property

获取形状中的第一个段落。

```csharp
public Paragraph FirstParagraph { get; }
```

## 例子

展示如何创建和格式化文本框。

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

// 向文本框添加一个段落并添加文本框将显示的一段文本。
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
