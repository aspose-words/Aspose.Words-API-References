---
title: PatternType Enum
linktitle: PatternType
articleTitle: PatternType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Drawing.PatternType, чтобы улучшить ваши фигуры с помощью настраиваемых шаблонов заливки. Улучшите дизайн вашего документа без усилий!
type: docs
weight: 1550
url: /ru/net/aspose.words.drawing/patterntype/
---
## PatternType enumeration

Указывает узор заливки, который будет использоваться для заливки фигуры.

```csharp
public enum PatternType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `-1` | Нет шаблона. |
| Percent10 | `1` | 10% цвета переднего плана. |
| Percent20 | `2` | 20% цвета переднего плана. |
| Percent25 | `3` | 25% цвета переднего плана. |
| Percent30 | `4` | 30% цвета переднего плана. |
| Percent40 | `5` | 40% цвета переднего плана |
| Percent50 | `6` | 50% цвета переднего плана |
| Percent5 | `7` | 5% цвета переднего плана. |
| Percent60 | `8` | 60% цвета переднего плана. |
| Percent70 | `9` | 70% цвета переднего плана. |
| Percent75 | `10` | 75% цвета переднего плана. |
| Percent80 | `11` | 80% цвета переднего плана. |
| Percent90 | `12` | 90% цвета переднего плана. |
| Cross | `13` | Крест. |
| DarkDownwardDiagonal | `14` | Темная диагональ вниз. |
| DarkHorizontal | `15` | Темный горизонтальный. |
| DarkUpwardDiagonal | `16` | Темная восходящая диагональ. |
| DarkVertical | `17` | Темная вертикаль. |
| DashedDownwardDiagonal | `18` | Пунктирная диагональ вниз. |
| DashedHorizontal | `19` | Горизонтальная пунктирная линия. |
| DashedUpwardDiagonal | `20` | Пунктирная восходящая диагональ. |
| DashedVertical | `21` | Вертикальная пунктирная линия. |
| DiagonalBrick | `22` | Диагональный кирпич. |
| DiagonalCross | `23` | Диагональный крест. |
| Divot | `24` | Узор divot. |
| DottedDiamond | `25` | Точечный ромб. |
| DottedGrid | `26` | Точечная сетка. |
| DownwardDiagonal | `27` | Нисходящая диагональ. |
| Horizontal | `28` | Горизонтально. |
| HorizontalBrick | `29` | Горизонтальный кирпич. |
| LargeCheckerBoard | `30` | Большая шахматная доска. |
| LargeConfetti | `31` | Большое конфетти. |
| LargeGrid | `32` | Большая сетка. |
| LightDownwardDiagonal | `33` | Светлая диагональ вниз. |
| LightHorizontal | `34` | Светлый горизонтальный. |
| LightUpwardDiagonal | `36` | Светлая восходящая диагональ. |
| LightVertical | `37` | Свет вертикальный. |
| NarrowHorizontal | `38` | Узкий горизонтальный. |
| NarrowVertical | `39` | Узкий вертикальный. |
| OutlinedDiamond | `40` | Очерченный ромб. |
| Plaid | `41` | Плед. |
| Shingle | `42` | Дранка. |
| SmallCheckerBoard | `43` | Маленькая шахматная доска. |
| SmallConfetti | `44` | Маленькое конфетти. |
| SmallGrid | `45` | Маленькая сетка. |
| SolidDiamond | `46` | Сплошной алмаз. |
| Sphere | `47` | Сфера. |
| Trellis | `48` | Решетка. |
| UpwardDiagonal | `49` | Восходящая диагональ. |
| Vertical | `50` | Вертикальный. |
| Wave | `51` | Волна. |
| Weave | `52` | Плетение. |
| WideDownwardDiagonal | `53` | Широкая диагональ вниз. |
| WideUpwardDiagonal | `54` | Широкая восходящая диагональ. |
| ZigZag | `55` | Зигзаг. |

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

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
