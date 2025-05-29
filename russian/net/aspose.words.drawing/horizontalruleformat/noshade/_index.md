---
title: HorizontalRuleFormat.NoShade
linktitle: NoShade
articleTitle: NoShade
second_title: Aspose.Words для .NET
description: Откройте для себя свойство HorizontalRuleFormat NoShade, управляйте 3D-затенением для горизонтальных линий. Получите гладкий, сплошной цветовой дизайн без усилий!
type: docs
weight: 40
url: /ru/net/aspose.words.drawing/horizontalruleformat/noshade/
---
## HorizontalRuleFormat.NoShade property

Указывает на наличие 3D-затенения для горизонтальной линии. Если`истинный` , то горизонтальная линия не имеет 3D-затенения и используется сплошной цвет.

```csharp
public bool NoShade { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ`.

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
