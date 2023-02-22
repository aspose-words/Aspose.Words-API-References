---
title: HorizontalRuleFormat.Alignment
second_title: Справочник по API Aspose.Words для .NET
description: HorizontalRuleFormat свойство. Получает или задает выравнивание горизонтальной линейки.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing/horizontalruleformat/alignment/
---
## HorizontalRuleFormat.Alignment property

Получает или задает выравнивание горизонтальной линейки.

```csharp
public HorizontalRuleAlignment Alignment { get; set; }
```

### Примечания

Значение по умолчаниюLeft.

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

* enum [HorizontalRuleAlignment](../../horizontalrulealignment/)
* class [HorizontalRuleFormat](../)
* пространство имен [Aspose.Words.Drawing](../../horizontalruleformat/)
* сборка [Aspose.Words](../../../)


