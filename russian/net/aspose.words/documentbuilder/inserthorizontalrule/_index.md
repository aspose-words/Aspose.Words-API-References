---
title: DocumentBuilder.InsertHorizontalRule
linktitle: InsertHorizontalRule
articleTitle: InsertHorizontalRule
second_title: Aspose.Words для .NET
description: Улучшите свои документы с помощью метода InsertHorizontalRule в DocumentBuilder, легко добавляя стильные горизонтальные линии для лучшей организации и визуальной привлекательности.
type: docs
weight: 370
url: /ru/net/aspose.words/documentbuilder/inserthorizontalrule/
---
## DocumentBuilder.InsertHorizontalRule method

Вставляет в документ горизонтальную линейку.

```csharp
public Shape InsertHorizontalRule()
```

### Возвращаемое значение

Форма, представляющая собой горизонтальную линейку.

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

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
