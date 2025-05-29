---
title: Story.FirstParagraph
linktitle: FirstParagraph
articleTitle: FirstParagraph
second_title: Aspose.Words for .NET
description: 发现 Story FirstParagraph 属性，轻松提取任何故事的第一段，增强您的内容和用户参与度。
type: docs
weight: 10
url: /zh/net/aspose.words/story/firstparagraph/
---
## Story.FirstParagraph property

获取故事的第一段。

```csharp
public Paragraph FirstParagraph { get; }
```

## 例子

展示如何使用字体属性来格式化文本。

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

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

* class [Paragraph](../../paragraph/)
* class [Story](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
