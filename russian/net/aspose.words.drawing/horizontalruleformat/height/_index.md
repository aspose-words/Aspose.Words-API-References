---
title: HorizontalRuleFormat.Height
linktitle: Height
articleTitle: Height
second_title: Aspose.Words для .NET
description: Легко настройте высоту вашего Горизонтального правила. Изучите свойство Height для настраиваемого дизайна в ваших веб-проектах. Улучшите свой макет сегодня!
type: docs
weight: 30
url: /ru/net/aspose.words.drawing/horizontalruleformat/height/
---
## HorizontalRuleFormat.Height property

Возвращает или задает высоту горизонтальной линейки.

```csharp
public double Height { get; set; }
```

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentOutOfRangeException | Вызывается, когда аргумент выходит за пределы допустимых значений. |

## Примечания

Это ярлык для[`Height`](../../shapebase/height/) свойство.

Допустимые значения находятся в диапазоне от 0 до 1584 включительно.

Значение по умолчанию — 1,5.

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
