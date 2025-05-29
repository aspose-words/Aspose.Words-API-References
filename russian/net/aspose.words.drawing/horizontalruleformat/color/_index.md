---
title: HorizontalRuleFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words для .NET
description: Откройте для себя свойство HorizontalRuleFormat Color, чтобы настроить свой дизайн. Легко установите или получите цвет кисти для потрясающего эффекта горизонтальной линии!
type: docs
weight: 20
url: /ru/net/aspose.words.drawing/horizontalruleformat/color/
---
## HorizontalRuleFormat.Color property

Получает или задает цвет кисти, заполняющей горизонтальную линейку.

```csharp
public Color Color { get; set; }
```

## Примечания

Это ярлык для[`Color`](../../fill/color/) свойство.

Значение по умолчанию: Gray .

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
