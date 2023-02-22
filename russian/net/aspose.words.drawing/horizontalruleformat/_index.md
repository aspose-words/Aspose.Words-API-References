---
title: Class HorizontalRuleFormat
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.HorizontalRuleFormat сорт. Представляет форматирование горизонтальной линейки.
type: docs
weight: 920
url: /ru/net/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class

Представляет форматирование горизонтальной линейки.

```csharp
public class HorizontalRuleFormat
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Alignment](../../aspose.words.drawing/horizontalruleformat/alignment/) { get; set; } | Получает или задает выравнивание горизонтальной линейки. |
| [Color](../../aspose.words.drawing/horizontalruleformat/color/) { get; set; } | Получает или задает цвет кисти, заполняющий горизонтальную линейку. |
| [Height](../../aspose.words.drawing/horizontalruleformat/height/) { get; set; } | Получает или задает высоту горизонтальной линейки. |
| [NoShade](../../aspose.words.drawing/horizontalruleformat/noshade/) { get; set; } | Указывает на наличие трехмерного затенения для горизонтальной линейки. Если true, то горизонтальная линейка не имеет трехмерного затенения и используется сплошной цвет. |
| [WidthPercent](../../aspose.words.drawing/horizontalruleformat/widthpercent/) { get; set; } | Получает или задает длину указанной горизонтальной линейки, выраженную в процентах от ширины окна. |

### Примеры

Показывает, как вставить фигуру горизонтальной линейки и настроить ее форматирование.

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

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)


