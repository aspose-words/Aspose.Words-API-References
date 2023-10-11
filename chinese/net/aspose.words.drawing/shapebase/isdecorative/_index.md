---
title: ShapeBase.IsDecorative
second_title: Aspose.Words for .NET API 参考
description: ShapeBase 财产. 获取或设置指定形状在文档中是否为装饰性的标志
type: docs
weight: 240
url: /zh/net/aspose.words.drawing/shapebase/isdecorative/
---
## ShapeBase.IsDecorative property

获取或设置指定形状在文档中是否为装饰性的标志。

```csharp
public bool IsDecorative { get; set; }
```

### 评论

请注意，形状不为空[`AlternativeText`](../alternativetext/)不能是装饰性的。

### 例子

展示如何设置形状具有装饰性。

```csharp
Document doc = new Document(MyDir + "Decorative shapes.docx");

Shape shape = (Shape) doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(shape.IsDecorative);

// 如果“AlternativeText”不为空，则形状不能是装饰性的。
// 这就是为什么我们的值已更改为“false”。
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
* 命名空间 [Aspose.Words.Drawing](../../shapebase/)
* 部件 [Aspose.Words](../../../)


