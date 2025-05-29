---
title: Adjustment.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Adjustment Value, легко получайте или задавайте необработанные значения корректировки, чтобы улучшить управление данными и оптимизировать процессы.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing/adjustment/value/
---
## Adjustment.Value property

Получает или задает необработанное значение корректировки.

```csharp
public int Value { get; set; }
```

## Примечания

Значение корректировки — это просто руководство, в котором указана формула на основе значения. То есть для руководства по значению корректировки не выполняется никаких расчетов. Вместо этого это руководство указывает значение параметра, которое используется для расчетов в рамках руководств формы.

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

* class [Adjustment](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
