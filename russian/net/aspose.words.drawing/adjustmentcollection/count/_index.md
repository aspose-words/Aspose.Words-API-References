---
title: AdjustmentCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words для .NET
description: Откройте для себя свойство AdjustmentCollection Count, чтобы легко получить общее количество элементов и повысить эффективность управления данными.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing/adjustmentcollection/count/
---
## AdjustmentCollection.Count property

Получает количество элементов, содержащихся в коллекции.

```csharp
public int Count { get; }
```

## Примеры

Показывает, как работать с исходными значениями корректировки.

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

### Смотрите также

* class [AdjustmentCollection](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
