---
title: AdjustmentCollection Class
linktitle: AdjustmentCollection
articleTitle: AdjustmentCollection
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.AdjustmentCollection 类——管理形状只读调整值的解决方案。轻松增强您的文档设计！
type: docs
weight: 710
url: /zh/net/aspose.words.drawing/adjustmentcollection/
---
## AdjustmentCollection class

表示只读集合[`Adjustment`](../adjustment/)调整应用于指定形状的值。

```csharp
public class AdjustmentCollection
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.drawing/adjustmentcollection/count/) { get; } | 获取集合中包含的元素数量。 |
| [Item](../../aspose.words.drawing/adjustmentcollection/item/) { get; } | 返回指定索引处的调整。 |

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

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
