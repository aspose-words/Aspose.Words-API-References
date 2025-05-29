---
title: ShapeBase.IsDecorative
linktitle: IsDecorative
articleTitle: IsDecorative
second_title: Aspose.Words for .NET
description: 探索 ShapeBase。轻松管理文档中的装饰属性。通过设置独特形状设计的标记，增强视觉吸引力。
type: docs
weight: 260
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

展示如何设置形状的装饰性。

```csharp
Document doc = new Document(MyDir + "Decorative shapes.docx");

Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(shape.IsDecorative);

// 如果“AlternativeText”不为空，则该形状不能具有装饰性。
// 这就是为什么我们的值变为“false”的原因。
shape.AlternativeText = "Alternative text.";
Assert.False(shape.IsDecorative);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
// 创建一个新的形状作为装饰。
shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.IsDecorative = true;

doc.Save(ArtifactsDir + "Shape.IsDecorative.docx");
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
