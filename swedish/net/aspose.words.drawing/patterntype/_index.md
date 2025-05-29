---
title: PatternType Enum
linktitle: PatternType
articleTitle: PatternType
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Drawing.PatternType-uppräkningen för att förbättra dina former med anpassningsbara fyllningsmönster. Förbättra din dokumentdesign utan ansträngning!
type: docs
weight: 1550
url: /sv/net/aspose.words.drawing/patterntype/
---
## PatternType enumeration

Anger fyllningsmönstret som ska användas för att fylla en form.

```csharp
public enum PatternType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `-1` | Inget mönster. |
| Percent10 | `1` | 10 % av förgrundsfärgen. |
| Percent20 | `2` | 20 % av förgrundsfärgen. |
| Percent25 | `3` | 25 % av förgrundsfärgen. |
| Percent30 | `4` | 30 % av förgrundsfärgen. |
| Percent40 | `5` | 40 % av förgrundsfärgen |
| Percent50 | `6` | 50 % av förgrundsfärgen |
| Percent5 | `7` | 5 % av förgrundsfärgen. |
| Percent60 | `8` | 60 % av förgrundsfärgen. |
| Percent70 | `9` | 70 % av förgrundsfärgen. |
| Percent75 | `10` | 75 % av förgrundsfärgen. |
| Percent80 | `11` | 80 % av förgrundsfärgen. |
| Percent90 | `12` | 90 % av förgrundsfärgen. |
| Cross | `13` | Kors. |
| DarkDownwardDiagonal | `14` | Mörk nedåtgående diagonal. |
| DarkHorizontal | `15` | Mörk horisontell. |
| DarkUpwardDiagonal | `16` | Mörk uppåtgående diagonal. |
| DarkVertical | `17` | Mörk vertikal. |
| DashedDownwardDiagonal | `18` | Streckad nedåtgående diagonal. |
| DashedHorizontal | `19` | Streckad horisontell. |
| DashedUpwardDiagonal | `20` | Streckad uppåtgående diagonal. |
| DashedVertical | `21` | Streckad vertikal. |
| DiagonalBrick | `22` | Diagonal tegelsten. |
| DiagonalCross | `23` | Diagonalt kors. |
| Divot | `24` | Mönsterduv. |
| DottedDiamond | `25` | Prickad diamant. |
| DottedGrid | `26` | Punkterat rutnät. |
| DownwardDiagonal | `27` | Nedåtgående diagonal. |
| Horizontal | `28` | Horisontell. |
| HorizontalBrick | `29` | Horisontell tegelsten. |
| LargeCheckerBoard | `30` | Stort schackbräde. |
| LargeConfetti | `31` | Stor konfetti. |
| LargeGrid | `32` | Stort rutnät. |
| LightDownwardDiagonal | `33` | Ljus nedåtgående diagonal. |
| LightHorizontal | `34` | Ljus horisontellt. |
| LightUpwardDiagonal | `36` | Ljus uppåtgående diagonal. |
| LightVertical | `37` | Ljus vertikal. |
| NarrowHorizontal | `38` | Smal horisontell. |
| NarrowVertical | `39` | Smal vertikal. |
| OutlinedDiamond | `40` | Konturerad diamant. |
| Plaid | `41` | Pläd. |
| Shingle | `42` | Bältros. |
| SmallCheckerBoard | `43` | Litet schackbräde. |
| SmallConfetti | `44` | Liten konfetti. |
| SmallGrid | `45` | Litet rutnät. |
| SolidDiamond | `46` | Solid diamant. |
| Sphere | `47` | Sfär. |
| Trellis | `48` | Spaljé. |
| UpwardDiagonal | `49` | Uppåtgående diagonal. |
| Vertical | `50` | Vertikal. |
| Wave | `51` | Våg. |
| Weave | `52` | Väva. |
| WideDownwardDiagonal | `53` | Bred nedåtgående diagonal. |
| WideUpwardDiagonal | `54` | Bred uppåtgående diagonal. |
| ZigZag | `55` | Sicksack. |

## Exempel

Visar hur man ställer in mönster för en form.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// Det finns flera sätt att ange fyllning i ett mönster.
// 1 - Applicera mönster på formfyllningen:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - Applicera mönster med förgrunds- och bakgrundsfärger på formfyllningen:
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### Se även

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
