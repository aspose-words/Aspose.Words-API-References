---
title: ShapeBase.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words for .NET
description: 探索 ShapeBase Font 属性，轻松访问字体格式。使用可自定义的文本样式和独特的排版选项，提升您的设计体验。
type: docs
weight: 190
url: /zh/net/aspose.words.drawing/shapebase/font/
---
## ShapeBase.Font property

提供对此对象的字体格式的访问。

```csharp
public Font Font { get; }
```

## 例子

展示如何插入文本框并设置其内容的字体。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.TextBox, 300, 50);
builder.MoveTo(shape.LastParagraph);
builder.Write("This text is inside the text box.");

// 将形状的“Font”对象的“Hidden”属性设置为“true”，以隐藏文本框
// 并折叠它通常占据的空间。
// 将形状的“Font”对象的“Hidden”属性设置为“false”以使文本框可见。
shape.Font.Hidden = hideShape;

// 如果形状可见，我们将通过字体对象修改其外观。
if (!hideShape)
{
    shape.Font.HighlightColor = Color.LightGray;
    shape.Font.Color = Color.Red;
    shape.Font.Underline = Underline.Dash;
}

// 将构建器从文本框移回主文档。
builder.MoveTo(shape.ParentParagraph);

builder.Writeln("\nThis text is outside the text box.");

doc.Save(ArtifactsDir + "Shape.Font.docx");
```

### 也可以看看

* class [Font](../../../aspose.words/font/)
* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
