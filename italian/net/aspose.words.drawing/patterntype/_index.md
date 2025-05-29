---
title: PatternType Enum
linktitle: PatternType
articleTitle: PatternType
second_title: Aspose.Words per .NET
description: Scopri l'enumerazione Aspose.Words.Drawing.PatternType per migliorare le tue forme con motivi di riempimento personalizzabili. Migliora il design dei tuoi documenti senza sforzo!
type: docs
weight: 1550
url: /it/net/aspose.words.drawing/patterntype/
---
## PatternType enumeration

Specifica il motivo di riempimento da utilizzare per riempire una forma.

```csharp
public enum PatternType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `-1` | Nessuno schema. |
| Percent10 | `1` | 10% del colore di primo piano. |
| Percent20 | `2` | 20% del colore di primo piano. |
| Percent25 | `3` | 25% del colore di primo piano. |
| Percent30 | `4` | 30% del colore di primo piano. |
| Percent40 | `5` | 40% del colore di primo piano |
| Percent50 | `6` | 50% del colore di primo piano |
| Percent5 | `7` | 5% del colore di primo piano. |
| Percent60 | `8` | 60% del colore di primo piano. |
| Percent70 | `9` | 70% del colore di primo piano. |
| Percent75 | `10` | 75% del colore di primo piano. |
| Percent80 | `11` | 80% del colore di primo piano. |
| Percent90 | `12` | 90% del colore di primo piano. |
| Cross | `13` | Croce. |
| DarkDownwardDiagonal | `14` | Diagonale scura verso il basso. |
| DarkHorizontal | `15` | Orizzontale scuro. |
| DarkUpwardDiagonal | `16` | Diagonale scura verso l'alto. |
| DarkVertical | `17` | Verticale scuro. |
| DashedDownwardDiagonal | `18` | Tratteggiato in diagonale verso il basso. |
| DashedHorizontal | `19` | Tratteggiato orizzontale. |
| DashedUpwardDiagonal | `20` | Tratteggiato in diagonale verso l'alto. |
| DashedVertical | `21` | Tratteggiato verticale. |
| DiagonalBrick | `22` | Mattone diagonale. |
| DiagonalCross | `23` | Croce diagonale. |
| Divot | `24` | Motivo a solco. |
| DottedDiamond | `25` | Diamante punteggiato. |
| DottedGrid | `26` | Griglia punteggiata. |
| DownwardDiagonal | `27` | Diagonale verso il basso. |
| Horizontal | `28` | Orizzontale. |
| HorizontalBrick | `29` | Mattone orizzontale. |
| LargeCheckerBoard | `30` | Grande scacchiera. |
| LargeConfetti | `31` | Grandi coriandoli. |
| LargeGrid | `32` | Griglia grande. |
| LightDownwardDiagonal | `33` | Leggera diagonale verso il basso. |
| LightHorizontal | `34` | Luce orizzontale. |
| LightUpwardDiagonal | `36` | Luce diagonale verso l'alto. |
| LightVertical | `37` | Luce verticale. |
| NarrowHorizontal | `38` | Orizzontale stretto. |
| NarrowVertical | `39` | Verticale stretto. |
| OutlinedDiamond | `40` | Diamante delineato. |
| Plaid | `41` | Plaid. |
| Shingle | `42` | Tegola. |
| SmallCheckerBoard | `43` | Piccola scacchiera. |
| SmallConfetti | `44` | Piccoli coriandoli. |
| SmallGrid | `45` | Griglia piccola. |
| SolidDiamond | `46` | Diamante massiccio. |
| Sphere | `47` | Sfera. |
| Trellis | `48` | Traliccio. |
| UpwardDiagonal | `49` | Diagonale verso l'alto. |
| Vertical | `50` | Verticale. |
| Wave | `51` | Onda. |
| Weave | `52` | Intrecciare. |
| WideDownwardDiagonal | `53` | Ampia diagonale verso il basso. |
| WideUpwardDiagonal | `54` | Ampia diagonale verso l'alto. |
| ZigZag | `55` | Zigzag. |

## Esempi

Mostra come impostare un pattern per una forma.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// Esistono diversi modi per specificare il riempimento di un pattern.
// 1 - Applica il motivo al riempimento della forma:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - Applica il motivo con colori di primo piano e di sfondo al riempimento della forma:
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
