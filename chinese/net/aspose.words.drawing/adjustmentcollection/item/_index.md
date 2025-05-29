---
title: AdjustmentCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: 发现 AdjustmentCollection Item 属性，轻松通过索引检索调整，实现无缝数据管理和增强性能。
type: docs
weight: 20
url: /zh/net/aspose.words.drawing/adjustmentcollection/item/
---
## AdjustmentCollection indexer

返回指定索引处的调整。

```csharp
public Adjustment this[int index] { get; }
```

| 范围 | 描述 |
| --- | --- |
| index | 集合的索引。 |

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

* class [Adjustment](../../adjustment/)
* class [AdjustmentCollection](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
