---
title: HorizontalRuleFormat.Alignment
linktitle: Alignment
articleTitle: Alignment
second_title: Aspose.Words для .NET
description: Откройте для себя свойство выравнивания HorizontalRuleFormat, которое позволяет легко настраивать выравнивание горизонтальных линий для повышения гибкости дизайна.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing/horizontalruleformat/alignment/
---
## HorizontalRuleFormat.Alignment property

Получает или задает выравнивание горизонтальной линии.

```csharp
public HorizontalRuleAlignment Alignment { get; set; }
```

## Примечания

Значение по умолчанию:Left.

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

* enum [HorizontalRuleAlignment](../../horizontalrulealignment/)
* class [HorizontalRuleFormat](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
