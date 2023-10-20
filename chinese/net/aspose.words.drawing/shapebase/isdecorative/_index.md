---
title: ShapeBase.IsDecorative
linktitle: IsDecorative
articleTitle: IsDecorative
second_title: 用于 .NET 的 Aspose.Words
description: ShapeBase IsDecorative 财产. 获取或设置指定形状在文档中是否具有装饰性的标志 在 C#.
type: docs
weight: 240
url: /zh/net/aspose.words.drawing/shapebase/isdecorative/
---
## ShapeBase.IsDecorative property

获取或设置指定形状在文档中是否具有装饰性的标志。

```csharp
public bool IsDecorative { get; set; }
```

## 评论

注意形状不为空[`AlternativeText`](../alternativetext/)不能是装饰性的。

## 例子

显示如何设置形状是装饰性的。

```csharp
Document doc = new Document(MyDir + "Decorative shapes.docx");

Shape shape = (Shape) doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(shape.IsDecorative);

// 如果“AlternativeText”不为空，则该形状不能是装饰性的。
// 这就是我们的值更改为“false”的原因。
shape.AlternativeText = "Alternative text.";
Assert.False(shape.IsDecorative);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
// 创建一个新形状作为装饰。
shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.IsDecorative = true;

doc.Save(ArtifactsDir + "Shape.IsDecorative.docx");
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
