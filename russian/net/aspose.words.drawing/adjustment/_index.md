---
title: Adjustment Class
linktitle: Adjustment
articleTitle: Adjustment
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.Adjustment, разработанный для улучшения ваших фигур с помощью точных значений настройки для превосходного форматирования документов.
type: docs
weight: 700
url: /ru/net/aspose.words.drawing/adjustment/
---
## Adjustment class

Представляет значения корректировки, применяемые к указанной форме.

```csharp
public class Adjustment
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Name](../../aspose.words.drawing/adjustment/name/) { get; } | Получает имя корректировки. |
| [Value](../../aspose.words.drawing/adjustment/value/) { get; set; } | Получает или задает необработанное значение корректировки. |

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
