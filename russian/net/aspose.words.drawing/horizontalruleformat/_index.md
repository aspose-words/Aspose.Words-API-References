---
title: HorizontalRuleFormat Class
linktitle: HorizontalRuleFormat
articleTitle: HorizontalRuleFormat
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.HorizontalRuleFormat для расширенного форматирования горизонтальных линий. Улучшите дизайн вашего документа без усилий!
type: docs
weight: 1380
url: /ru/net/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class

Представляет форматирование горизонтальной линии.

Чтобы узнать больше, посетите[Работа с фигурами](https://docs.aspose.com/words/net/working-with-shapes/) документальная статья.

```csharp
public class HorizontalRuleFormat
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Alignment](../../aspose.words.drawing/horizontalruleformat/alignment/) { get; set; } | Получает или задает выравнивание горизонтальной линии. |
| [Color](../../aspose.words.drawing/horizontalruleformat/color/) { get; set; } | Получает или задает цвет кисти, заполняющей горизонтальную линейку. |
| [Height](../../aspose.words.drawing/horizontalruleformat/height/) { get; set; } | Возвращает или задает высоту горизонтальной линейки. |
| [NoShade](../../aspose.words.drawing/horizontalruleformat/noshade/) { get; set; } | Указывает на наличие 3D-затенения для горизонтальной линии. Если`истинный` , то горизонтальная линия не имеет 3D-затенения и используется сплошной цвет. |
| [WidthPercent](../../aspose.words.drawing/horizontalruleformat/widthpercent/) { get; set; } | Возвращает или задает длину указанной горизонтальной линии, выраженную в процентах от ширины окна. |

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

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
