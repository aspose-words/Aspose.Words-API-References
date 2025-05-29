---
title: ShapeBase.IsHorizontalRule
linktitle: IsHorizontalRule
articleTitle: IsHorizontalRule
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase IsHorizontalRule, с легкостью определяйте горизонтальные линии в своих проектах для улучшения эффективности компоновки и стилизации.
type: docs
weight: 290
url: /ru/net/aspose.words.drawing/shapebase/ishorizontalrule/
---
## ShapeBase.IsHorizontalRule property

Возврат`истинный` если эта фигура является горизонтальной линейкой.

```csharp
public bool IsHorizontalRule { get; }
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

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
