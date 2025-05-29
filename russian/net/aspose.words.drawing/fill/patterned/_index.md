---
title: Fill.Patterned
linktitle: Patterned
articleTitle: Patterned
second_title: Aspose.Words для .NET
description: Откройте для себя метод Fill Patterned, позволяющий с легкостью применять уникальные узоры к вашим проектам, повышая их креативность и визуальную привлекательность.
type: docs
weight: 230
url: /ru/net/aspose.words.drawing/fill/patterned/
---
## Patterned(*[PatternType](../../patterntype/)*) {#patterned}

Устанавливает указанную заливку в соответствии с шаблоном.

```csharp
public void Patterned(PatternType patternType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |

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

---

## Patterned(*[PatternType](../../patterntype/), Color, Color*) {#patterned_1}

Устанавливает указанную заливку в соответствии с шаблоном.

```csharp
public void Patterned(PatternType patternType, Color foreColor, Color backColor)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |
| foreColor | Color | Цвет заливки переднего плана. |
| backColor | Color | Цвет фоновой заливки. |

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
