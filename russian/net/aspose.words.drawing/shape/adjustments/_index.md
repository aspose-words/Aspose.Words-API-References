---
title: Shape.Adjustments
linktitle: Adjustments
articleTitle: Adjustments
second_title: Aspose.Words для .NET
description: Откройте для себя корректировки формы. Получите доступ к исходным значениям для точных изменений формы. Легко улучшайте дизайн с помощью индивидуальных корректировок для достижения оптимальных результатов.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing/shape/adjustments/
---
## Shape.Adjustments property

Предоставляет доступ к необработанным значениям корректировки фигуры. Для фигуры, которая не содержит необработанных значений корректировки, возвращается пустая коллекция.

```csharp
public AdjustmentCollection Adjustments { get; }
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

* class [AdjustmentCollection](../../adjustmentcollection/)
* class [Shape](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
