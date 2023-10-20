---
title: Shape
linktitle: Shape
articleTitle: Shape
second_title: 用于 .NET 的 Aspose.Words
description: Shape 构造函数. 创建一个新的形状对象 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.drawing/shape/shape/
---
## Shape constructor

创建一个新的形状对象。

```csharp
public Shape(DocumentBase doc, ShapeType shapeType)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | DocumentBase | 所有者文件。 |
| shapeType | ShapeType | 要创建的形状的类型。 |

## 评论

您应该在创建形状后指定所需的形状属性。

## 例子

演示如何将带有图像的形状从本地文件系统插入到文档中。

```csharp
Document doc = new Document();

// “Shape”类的公共构造函数将创建一个带有“ShapeMarkupLanguage.Vml”标记类型的形状。
// 如果需要创建非原始类型的形状，如 SingleCornerSnipped、TopCornersSnipped、DiagonalCornersSnipped、
// TopCornersOneRoundedOneSnipped、SingleCornerRounded、TopCornersRounded 或 DiagonalCornersRounded,
// 请使用 DocumentBuilder.InsertShape。
Shape shape = new Shape(doc, ShapeType.Image);
shape.ImageData.SetImage(ImageDir + "Windows MetaFile.wmf");
shape.Width = 100;
shape.Height = 100;

doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

doc.Save(ArtifactsDir + "Image.FromFile.docx");
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

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [ShapeType](../../shapetype/)
* class [Shape](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
