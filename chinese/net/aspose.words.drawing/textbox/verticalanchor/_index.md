---
title: TextBox.VerticalAnchor
second_title: Aspose.Words for .NET API 参考
description: TextBox 财产. 指定形状内文本的垂直对齐方式
type: docs
weight: 120
url: /zh/net/aspose.words.drawing/textbox/verticalanchor/
---
## TextBox.VerticalAnchor property

指定形状内文本的垂直对齐方式。

```csharp
public TextBoxAnchor VerticalAnchor { get; set; }
```

### 评论

默认值为Top。

### 例子

演示如何垂直对齐文本框的文本内容。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// 将“VerticalAnchor”属性设置为“TextBoxAnchor.Top”
// 将此文本框中的文本与形状的顶部对齐。
// 将“VerticalAnchor”属性设置为“TextBoxAnchor.Middle”
// 将此文本框中的文本与形状的中心对齐。
// 将“VerticalAnchor”属性设置为“TextBoxAnchor.Bottom”
// 将此文本框中的文本与形状的底部对齐。
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// 从 Microsoft Word 2007 开始，文本框中文本的垂直对齐功能可用。
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### 也可以看看

* enum [TextBoxAnchor](../../textboxanchor/)
* class [TextBox](../)
* 命名空间 [Aspose.Words.Drawing](../../textbox/)
* 部件 [Aspose.Words](../../../)


