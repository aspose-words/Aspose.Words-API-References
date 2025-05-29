---
title: HorizontalRuleFormat.WidthPercent
linktitle: WidthPercent
articleTitle: WidthPercent
second_title: Aspose.Words для .NET
description: Откройте для себя свойство HorizontalRuleFormat WidthPercent, чтобы легко настроить длину горизонтальной линейки в процентах от ширины окна для лучшего управления дизайном.
type: docs
weight: 50
url: /ru/net/aspose.words.drawing/horizontalruleformat/widthpercent/
---
## HorizontalRuleFormat.WidthPercent property

Возвращает или задает длину указанной горизонтальной линии, выраженную в процентах от ширины окна.

```csharp
public double WidthPercent { get; set; }
```

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentOutOfRangeException | Вызывается, когда аргумент выходит за пределы допустимых значений. |

## Примечания

Допустимые значения находятся в диапазоне от 1 до 100 включительно.

Значение по умолчанию — 100.

## Примеры

Показывает, как вставить горизонтальную линейку и настроить ее форматирование.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertHorizontalRule();

HorizontalRuleFormat horizontalRuleFormat = shape.HorizontalRuleFormat;
horizontalRuleFormat.Alignment = HorizontalRuleAlignment.Center;
horizontalRuleFormat.WidthPercent = 70;
horizontalRuleFormat.Height = 3;
horizontalRuleFormat.Color = Color.Blue;
horizontalRuleFormat.NoShade = true;

Assert.True(shape.IsHorizontalRule);
Assert.True(shape.HorizontalRuleFormat.NoShade);
```

### Смотрите также

* class [HorizontalRuleFormat](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
