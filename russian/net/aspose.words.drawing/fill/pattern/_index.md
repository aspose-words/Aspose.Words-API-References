---
title: Fill.Pattern
linktitle: Pattern
articleTitle: Pattern
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Fill Pattern, чтобы легко получить доступ к PatternType и настроить его для ваших проектов. Улучшите свои проекты с помощью уникальных вариантов заливки!
type: docs
weight: 160
url: /ru/net/aspose.words.drawing/fill/pattern/
---
## Fill.Pattern property

Получает[`PatternType`](../../patterntype/) для заполнения.

```csharp
public PatternType Pattern { get; }
```

## Примеры

Показывает, как задать узор для фигуры.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// Существует несколько способов задания заливки по шаблону.
// 1 - Применить узор к заливке фигуры:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - Применить узор с цветами переднего плана и фона к заливке фигуры:
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### Смотрите также

* enum [PatternType](../../patterntype/)
* class [Fill](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
