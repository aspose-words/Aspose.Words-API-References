---
title: AdjustmentCollection Class
linktitle: AdjustmentCollection
articleTitle: AdjustmentCollection
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.AdjustmentCollection — ваше решение для управления значениями корректировки только для чтения для фигур. Улучшайте дизайн своих документов без усилий!
type: docs
weight: 710
url: /ru/net/aspose.words.drawing/adjustmentcollection/
---
## AdjustmentCollection class

Представляет коллекцию, доступную только для чтения[`Adjustment`](../adjustment/) настроить значения, применяемые к указанной форме.

```csharp
public class AdjustmentCollection
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.drawing/adjustmentcollection/count/) { get; } | Получает количество элементов, содержащихся в коллекции. |
| [Item](../../aspose.words.drawing/adjustmentcollection/item/) { get; } | Возвращает корректировку по указанному индексу. |

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

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
