---
title: Story.FirstParagraph
second_title: Aspose.Words for .NET API 参考
description: Story 财产. 获取故事的第一段
type: docs
weight: 10
url: /zh/net/aspose.words/story/firstparagraph/
---
## Story.FirstParagraph property

获取故事的第一段。

```csharp
public Paragraph FirstParagraph { get; }
```

### 例子

显示如何使用其字体属性格式化文本运行。

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

演示如何创建和格式化文本框。

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

// 向文本框中添加一个段落，并添加文本框将显示的一连串文本。
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
* 命名空间 [Aspose.Words](../../story/)
* 部件 [Aspose.Words](../../../)


