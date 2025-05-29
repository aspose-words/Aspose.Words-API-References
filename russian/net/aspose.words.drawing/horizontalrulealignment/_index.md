---
title: HorizontalRuleAlignment Enum
linktitle: HorizontalRuleAlignment
articleTitle: HorizontalRuleAlignment
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.HorizontalRuleAlignment для точного управления горизонтальным выравниванием линий, улучшая форматирование и дизайн вашего документа.
type: docs
weight: 1370
url: /ru/net/aspose.words.drawing/horizontalrulealignment/
---
## HorizontalRuleAlignment enumeration

Представляет выравнивание для указанной горизонтальной линии.

```csharp
public enum HorizontalRuleAlignment
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Left | `0` | Выровнено по левому краю. |
| Center | `1` | Выровнено по центру. |
| Right | `2` | Выровнено по правому краю. |

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
