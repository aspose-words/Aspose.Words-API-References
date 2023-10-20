---
title: Fill.Patterned
linktitle: Patterned
articleTitle: Patterned
second_title: Aspose.Words для .NET
description: Fill Patterned метод. Устанавливает указанную заливку в шаблон на С#.
type: docs
weight: 220
url: /ru/net/aspose.words.drawing/fill/patterned/
---
## Patterned(*[PatternType](../../patterntype/)*) {#patterned}

Устанавливает указанную заливку в шаблон.

```csharp
public void Patterned(PatternType patternType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |

## Примеры

Показывает, как задать шаблон для фигуры.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// Существует несколько способов заполнения шаблона.
// 1 - Применить узор к заливке фигуры:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - Применить к заливке фигуры узор с цветами переднего плана и фона:
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

Устанавливает указанную заливку в шаблон.

```csharp
public void Patterned(PatternType patternType, Color foreColor, Color backColor)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |
| foreColor | Color | Цвет заливки переднего плана. |
| backColor | Color | Цвет заливки фона. |

## Примеры

Показывает, как задать шаблон для фигуры.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// Существует несколько способов заполнения шаблона.
// 1 - Применить узор к заливке фигуры:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - Применить к заливке фигуры узор с цветами переднего плана и фона:
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### Смотрите также

* enum [PatternType](../../patterntype/)
* class [Fill](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
