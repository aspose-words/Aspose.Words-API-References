---
title: HorizontalRuleFormat.NoShade
second_title: Справочник по API Aspose.Words для .NET
description: HorizontalRuleFormat свойство. Указывает на наличие трехмерного затенения для горизонтальной линейки. Если true то горизонтальная линейка не имеет трехмерного затенения и используется сплошной цвет.
type: docs
weight: 40
url: /ru/net/aspose.words.drawing/horizontalruleformat/noshade/
---
## HorizontalRuleFormat.NoShade property

Указывает на наличие трехмерного затенения для горизонтальной линейки. Если true, то горизонтальная линейка не имеет трехмерного затенения и используется сплошной цвет.

```csharp
public bool NoShade { get; set; }
```

### Примечания

Значение по умолчанию неверно.

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

* class [HorizontalRuleFormat](../)
* пространство имен [Aspose.Words.Drawing](../../horizontalruleformat/)
* сборка [Aspose.Words](../../../)


