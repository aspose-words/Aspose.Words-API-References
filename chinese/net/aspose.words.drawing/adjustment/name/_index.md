---
title: Adjustment.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words for .NET
description: 发现调整名称属性，以便轻松访问和管理您的调整，从而提高效率和简化工作流程。
type: docs
weight: 10
url: /zh/net/aspose.words.drawing/adjustment/name/
---
## Adjustment.Name property

获取调整的名称。

```csharp
public string Name { get; }
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

* class [Adjustment](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
