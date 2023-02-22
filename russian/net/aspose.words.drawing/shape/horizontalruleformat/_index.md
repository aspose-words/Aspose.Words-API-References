---
title: Shape.HorizontalRuleFormat
second_title: Справочник по API Aspose.Words для .NET
description: Shape свойство. Предоставляет доступ к свойствам фигуры горизонтальной линейки. Для фигуры не являющейся горизонтальной линейкой возвращает null.
type: docs
weight: 100
url: /ru/net/aspose.words.drawing/shape/horizontalruleformat/
---
## Shape.HorizontalRuleFormat property

Предоставляет доступ к свойствам фигуры горизонтальной линейки. Для фигуры, не являющейся горизонтальной линейкой, возвращает null.

```csharp
public HorizontalRuleFormat HorizontalRuleFormat { get; }
```

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

* class [HorizontalRuleFormat](../../horizontalruleformat/)
* class [Shape](../)
* пространство имен [Aspose.Words.Drawing](../../shape/)
* сборка [Aspose.Words](../../../)


