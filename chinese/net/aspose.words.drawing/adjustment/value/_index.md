---
title: Adjustment.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words for .NET
description: 发现调整值属性，轻松获取或设置原始调整值以增强数据管理并简化流程。
type: docs
weight: 20
url: /zh/net/aspose.words.drawing/adjustment/value/
---
## Adjustment.Value property

获取或设置调整的原始值。

```csharp
public int Value { get; set; }
```

## 评论

调整值仅仅是一个具有指定基于值的公式的指南。 也就是说，调整值指南不会进行任何计算。 相反，此指南指定用于形状指南内计算的参数值。

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

* class [Adjustment](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
