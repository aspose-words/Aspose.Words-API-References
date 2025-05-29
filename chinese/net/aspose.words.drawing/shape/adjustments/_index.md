---
title: Shape.Adjustments
linktitle: Adjustments
articleTitle: Adjustments
second_title: Aspose.Words for .NET
description: 探索形状调整。访问原始值，进行精确的形状修改。轻松通过定制调整来增强设计，获得最佳效果。
type: docs
weight: 20
url: /zh/net/aspose.words.drawing/shape/adjustments/
---
## Shape.Adjustments property

提供对形状的调整原始值的访问。 对于不包含任何调整原始值的形状，它将返回一个空集合。

```csharp
public AdjustmentCollection Adjustments { get; }
```

## 例子

展示如何使用调整原始值。

```csharp
Document doc = new Document(MyDir + "Rounded rectangle shape.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

AdjustmentCollection adjustments = shape.Adjustments;
Assert.AreEqual(1, adjustments.Count);

Adjustment adjustment = adjustments[0];
Assert.AreEqual("adj", adjustment.Name);
Assert.AreEqual(16667, adjustment.Value);

adjustment.Value = 30000;

doc.Save(ArtifactsDir + "Shape.Adjustments.docx");
```

### 也可以看看

* class [AdjustmentCollection](../../adjustmentcollection/)
* class [Shape](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
