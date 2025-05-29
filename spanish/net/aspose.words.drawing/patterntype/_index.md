---
title: PatternType Enum
linktitle: PatternType
articleTitle: PatternType
second_title: Aspose.Words para .NET
description: Descubre la enumeración Aspose.Words.Drawing.PatternType para mejorar tus formas con patrones de relleno personalizables. ¡Mejora el diseño de tus documentos sin esfuerzo!
type: docs
weight: 1550
url: /es/net/aspose.words.drawing/patterntype/
---
## PatternType enumeration

Especifica el patrón de relleno que se utilizará para rellenar una forma.

```csharp
public enum PatternType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `-1` | Sin patrón. |
| Percent10 | `1` | 10% del color de primer plano. |
| Percent20 | `2` | 20% del color de primer plano. |
| Percent25 | `3` | 25% del color de primer plano. |
| Percent30 | `4` | 30% del color de primer plano. |
| Percent40 | `5` | 40% del color de primer plano |
| Percent50 | `6` | 50% del color de primer plano |
| Percent5 | `7` | 5% del color de primer plano. |
| Percent60 | `8` | 60% del color de primer plano. |
| Percent70 | `9` | 70% del color de primer plano. |
| Percent75 | `10` | 75% del color de primer plano. |
| Percent80 | `11` | 80% del color de primer plano. |
| Percent90 | `12` | 90% del color de primer plano. |
| Cross | `13` | Cruz. |
| DarkDownwardDiagonal | `14` | Diagonal oscura hacia abajo. |
| DarkHorizontal | `15` | Horizontal oscuro. |
| DarkUpwardDiagonal | `16` | Diagonal oscura hacia arriba. |
| DarkVertical | `17` | Vertical oscuro. |
| DashedDownwardDiagonal | `18` | Diagonal discontinua hacia abajo. |
| DashedHorizontal | `19` | Trazado horizontal discontinuo. |
| DashedUpwardDiagonal | `20` | Diagonal discontinua hacia arriba. |
| DashedVertical | `21` | Trazos verticales. |
| DiagonalBrick | `22` | Ladrillo diagonal. |
| DiagonalCross | `23` | Cruz diagonal. |
| Divot | `24` | Punto de patrón. |
| DottedDiamond | `25` | Diamante punteado. |
| DottedGrid | `26` | Cuadrícula de puntos. |
| DownwardDiagonal | `27` | Diagonal hacia abajo. |
| Horizontal | `28` | Horizontal. |
| HorizontalBrick | `29` | Ladrillo horizontal. |
| LargeCheckerBoard | `30` | Tablero de ajedrez grande. |
| LargeConfetti | `31` | Confeti grande. |
| LargeGrid | `32` | Cuadrícula grande. |
| LightDownwardDiagonal | `33` | Luz diagonal hacia abajo. |
| LightHorizontal | `34` | Luz horizontal. |
| LightUpwardDiagonal | `36` | Luz diagonal ascendente. |
| LightVertical | `37` | Luz vertical. |
| NarrowHorizontal | `38` | Estrecho horizontal. |
| NarrowVertical | `39` | Vertical estrecho. |
| OutlinedDiamond | `40` | Diamante delineado. |
| Plaid | `41` | Cuadros. |
| Shingle | `42` | Teja. |
| SmallCheckerBoard | `43` | Pequeño tablero de ajedrez. |
| SmallConfetti | `44` | Confeti pequeño. |
| SmallGrid | `45` | Cuadrícula pequeña. |
| SolidDiamond | `46` | Diamante macizo. |
| Sphere | `47` | Esfera. |
| Trellis | `48` | Enrejado. |
| UpwardDiagonal | `49` | Diagonal hacia arriba. |
| Vertical | `50` | Vertical. |
| Wave | `51` | Ola. |
| Weave | `52` | Tejido. |
| WideDownwardDiagonal | `53` | Diagonal amplia hacia abajo. |
| WideUpwardDiagonal | `54` | Diagonal amplia hacia arriba. |
| ZigZag | `55` | Zigzag. |

## Ejemplos

Muestra cómo establecer un patrón para una forma.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

//Hay varias formas de rellenar un patrón especificado.
// 1 - Aplicar patrón al relleno de forma:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - Aplicar patrón con colores de primer plano y de fondo al relleno de la forma:
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
