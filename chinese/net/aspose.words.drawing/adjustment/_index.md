---
title: Adjustment Class
linktitle: Adjustment
articleTitle: Adjustment
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Adjustment 类，旨在通过精确的调整值增强您的形状，从而实现卓越的文档格式。
type: docs
weight: 700
url: /zh/net/aspose.words.drawing/adjustment/
---
## Adjustment class

表示应用于指定形状的调整值。

```csharp
public class Adjustment
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Name](../../aspose.words.drawing/adjustment/name/) { get; } | 获取调整的名称。 |
| [Value](../../aspose.words.drawing/adjustment/value/) { get; set; } | 获取或设置调整的原始值。 |

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
