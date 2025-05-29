---
title: PatternType Enum
linktitle: PatternType
articleTitle: PatternType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.Drawing.PatternType, um Ihre Formen mit anpassbaren Füllmustern zu verbessern. Verbessern Sie Ihr Dokumentdesign mühelos!
type: docs
weight: 1550
url: /de/net/aspose.words.drawing/patterntype/
---
## PatternType enumeration

Gibt das Füllmuster an, das zum Füllen einer Form verwendet werden soll.

```csharp
public enum PatternType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `-1` | Kein Muster. |
| Percent10 | `1` | 10 % der Vordergrundfarbe. |
| Percent20 | `2` | 20 % der Vordergrundfarbe. |
| Percent25 | `3` | 25 % der Vordergrundfarbe. |
| Percent30 | `4` | 30 % der Vordergrundfarbe. |
| Percent40 | `5` | 40 % der Vordergrundfarbe |
| Percent50 | `6` | 50 % der Vordergrundfarbe |
| Percent5 | `7` | 5 % der Vordergrundfarbe. |
| Percent60 | `8` | 60 % der Vordergrundfarbe. |
| Percent70 | `9` | 70 % der Vordergrundfarbe. |
| Percent75 | `10` | 75 % der Vordergrundfarbe. |
| Percent80 | `11` | 80 % der Vordergrundfarbe. |
| Percent90 | `12` | 90 % der Vordergrundfarbe. |
| Cross | `13` | Kreuz. |
| DarkDownwardDiagonal | `14` | Dunkel diagonal nach unten. |
| DarkHorizontal | `15` | Dunkel horizontal. |
| DarkUpwardDiagonal | `16` | Dunkel diagonal nach oben. |
| DarkVertical | `17` | Dunkle Vertikale. |
| DashedDownwardDiagonal | `18` | Gestrichelte Diagonale nach unten. |
| DashedHorizontal | `19` | Horizontal gestrichelt. |
| DashedUpwardDiagonal | `20` | Gestrichelte Diagonale nach oben. |
| DashedVertical | `21` | Gestrichelte Vertikale. |
| DiagonalBrick | `22` | Diagonaler Ziegelstein. |
| DiagonalCross | `23` | Diagonales Kreuz. |
| Divot | `24` | Muster-Divot. |
| DottedDiamond | `25` | Gepunktete Raute. |
| DottedGrid | `26` | Gepunktetes Gitter. |
| DownwardDiagonal | `27` | Diagonal nach unten. |
| Horizontal | `28` | Horizontal. |
| HorizontalBrick | `29` | Horizontaler Ziegelstein. |
| LargeCheckerBoard | `30` | Großes Schachbrett. |
| LargeConfetti | `31` | Großes Konfetti. |
| LargeGrid | `32` | Großes Gitter. |
| LightDownwardDiagonal | `33` | Licht diagonal nach unten. |
| LightHorizontal | `34` | Licht horizontal. |
| LightUpwardDiagonal | `36` | Licht diagonal nach oben. |
| LightVertical | `37` | Licht vertikal. |
| NarrowHorizontal | `38` | Schmal horizontal. |
| NarrowVertical | `39` | Schmale Vertikale. |
| OutlinedDiamond | `40` | Umrandeter Diamant. |
| Plaid | `41` | Kariert. |
| Shingle | `42` | Schindel. |
| SmallCheckerBoard | `43` | Kleines Schachbrett. |
| SmallConfetti | `44` | Kleines Konfetti. |
| SmallGrid | `45` | Kleines Gitter. |
| SolidDiamond | `46` | Massiver Diamant. |
| Sphere | `47` | Kugel. |
| Trellis | `48` | Gitter. |
| UpwardDiagonal | `49` | Diagonal nach oben. |
| Vertical | `50` | Vertikal. |
| Wave | `51` | Welle. |
| Weave | `52` | Weben. |
| WideDownwardDiagonal | `53` | Breit diagonal nach unten. |
| WideUpwardDiagonal | `54` | Breit diagonal nach oben. |
| ZigZag | `55` | Zickzack. |

## Beispiele

Zeigt, wie man ein Muster für eine Form festlegt.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// Es gibt mehrere Möglichkeiten, ein Muster mit einer bestimmten Füllung zu versehen.
// 1 - Muster auf die Formfüllung anwenden:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - Muster mit Vordergrund- und Hintergrundfarben auf die Formfüllung anwenden:
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
