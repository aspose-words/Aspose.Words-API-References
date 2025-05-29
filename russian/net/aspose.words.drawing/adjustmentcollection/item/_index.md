---
title: AdjustmentCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: Откройте для себя свойство AdjustmentCollection Item, легко извлекайте корректировки по индексу для бесперебойного управления данными и повышения производительности.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing/adjustmentcollection/item/
---
## AdjustmentCollection indexer

Возвращает корректировку по указанному индексу.

```csharp
public Adjustment this[int index] { get; }
```

| Параметр | Описание |
| --- | --- |
| index | Указатель коллекции. |

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

* class [Adjustment](../../adjustment/)
* class [AdjustmentCollection](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
