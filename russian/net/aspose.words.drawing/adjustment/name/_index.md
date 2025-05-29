---
title: Adjustment.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words для .NET
description: Откройте для себя свойство «Имя корректировки», чтобы легко получать доступ к корректировкам и управлять ими для повышения эффективности и оптимизации рабочих процессов.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing/adjustment/name/
---
## Adjustment.Name property

Получает имя корректировки.

```csharp
public string Name { get; }
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

* class [Adjustment](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
