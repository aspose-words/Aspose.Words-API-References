---
title: Shape.HorizontalRuleFormat
linktitle: HorizontalRuleFormat
articleTitle: HorizontalRuleFormat
second_title: Aspose.Words для .NET
description: Доступ и настройка свойств HorizontalRuleFormat для повышения гибкости дизайна. Оптимизируйте свои формы с помощью индивидуальных настроек для уникальных результатов.
type: docs
weight: 110
url: /ru/net/aspose.words.drawing/shape/horizontalruleformat/
---
## Shape.HorizontalRuleFormat property

Предоставляет доступ к свойствам формы горизонтальной линейки. Для формы, которая не является горизонтальной линейкой, возвращает`нулевой` .

```csharp
public HorizontalRuleFormat HorizontalRuleFormat { get; }
```

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

* class [HorizontalRuleFormat](../../horizontalruleformat/)
* class [Shape](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
