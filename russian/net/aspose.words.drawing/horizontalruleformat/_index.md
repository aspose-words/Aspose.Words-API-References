---
title: Class HorizontalRuleFormat
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.HorizontalRuleFormat сорт. Представляет горизонтальное форматирование правил.
type: docs
weight: 1050
url: /ru/net/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class

Представляет горизонтальное форматирование правил.

Чтобы узнать больше, посетите[Работа с фигурами](https://docs.aspose.com/words/net/working-with-shapes/) статья документации.

```csharp
public class HorizontalRuleFormat
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Alignment](../../aspose.words.drawing/horizontalruleformat/alignment/) { get; set; } | Получает или задает выравнивание горизонтальной линейки. |
| [Color](../../aspose.words.drawing/horizontalruleformat/color/) { get; set; } | Получает или задает цвет кисти, заполняющий горизонтальное правило. |
| [Height](../../aspose.words.drawing/horizontalruleformat/height/) { get; set; } | Получает или задает высоту горизонтальной линейки. |
| [NoShade](../../aspose.words.drawing/horizontalruleformat/noshade/) { get; set; } | Указывает наличие 3D-затенения для горизонтальной линейки. Если`истинный` то горизонтальная линейка без 3D-затенения и используется сплошной цвет. |
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


