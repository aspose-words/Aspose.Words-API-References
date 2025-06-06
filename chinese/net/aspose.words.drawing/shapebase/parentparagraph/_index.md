---
title: ShapeBase.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: Aspose.Words for .NET
description: 发现 ShapeBase ParentParagraph 属性——有效访问直接父段落，以简化内容管理和增强组织。
type: docs
weight: 430
url: /zh/net/aspose.words.drawing/shapebase/parentparagraph/
---
## ShapeBase.ParentParagraph property

返回直接父段落。

```csharp
public Paragraph ParentParagraph { get; }
```

## 评论

对于组形状的子形状和 Office Math 对象的子形状始终返回`无效的`。

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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
