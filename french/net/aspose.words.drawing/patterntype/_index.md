---
title: PatternType Enum
linktitle: PatternType
articleTitle: PatternType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Drawing.PatternType pour enrichir vos formes avec des motifs de remplissage personnalisables. Améliorez la conception de vos documents sans effort !
type: docs
weight: 1550
url: /fr/net/aspose.words.drawing/patterntype/
---
## PatternType enumeration

Spécifie le motif de remplissage à utiliser pour remplir une forme.

```csharp
public enum PatternType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `-1` | Aucun motif. |
| Percent10 | `1` | 10% de la couleur de premier plan. |
| Percent20 | `2` | 20% de la couleur de premier plan. |
| Percent25 | `3` | 25% de la couleur de premier plan. |
| Percent30 | `4` | 30% de la couleur de premier plan. |
| Percent40 | `5` | 40% de la couleur de premier plan |
| Percent50 | `6` | 50% de la couleur de premier plan |
| Percent5 | `7` | 5% de la couleur de premier plan. |
| Percent60 | `8` | 60% de la couleur de premier plan. |
| Percent70 | `9` | 70% de la couleur de premier plan. |
| Percent75 | `10` | 75% de la couleur de premier plan. |
| Percent80 | `11` | 80% de la couleur de premier plan. |
| Percent90 | `12` | 90% de la couleur de premier plan. |
| Cross | `13` | Croix. |
| DarkDownwardDiagonal | `14` | Diagonale sombre vers le bas. |
| DarkHorizontal | `15` | Horizontal foncé. |
| DarkUpwardDiagonal | `16` | Diagonale sombre vers le haut. |
| DarkVertical | `17` | Verticale sombre. |
| DashedDownwardDiagonal | `18` | Diagonale pointillée vers le bas. |
| DashedHorizontal | `19` | Pointillés horizontaux. |
| DashedUpwardDiagonal | `20` | Diagonale pointillée vers le haut. |
| DashedVertical | `21` | Pointillés verticaux. |
| DiagonalBrick | `22` | Brique diagonale. |
| DiagonalCross | `23` | Croix diagonale. |
| Divot | `24` | Motif divot. |
| DottedDiamond | `25` | Losange en pointillé. |
| DottedGrid | `26` | Grille en pointillés. |
| DownwardDiagonal | `27` | Diagonale vers le bas. |
| Horizontal | `28` | Horizontale. |
| HorizontalBrick | `29` | Brique horizontale. |
| LargeCheckerBoard | `30` | Grand damier. |
| LargeConfetti | `31` | Gros confettis. |
| LargeGrid | `32` | Grande grille. |
| LightDownwardDiagonal | `33` | Lumière diagonale vers le bas. |
| LightHorizontal | `34` | Lumière horizontale. |
| LightUpwardDiagonal | `36` | Lumière diagonale vers le haut. |
| LightVertical | `37` | Lumière verticale. |
| NarrowHorizontal | `38` | Horizontal étroit. |
| NarrowVertical | `39` | Verticale étroite. |
| OutlinedDiamond | `40` | Losange souligné. |
| Plaid | `41` | Plaid. |
| Shingle | `42` | Bardeau. |
| SmallCheckerBoard | `43` | Petit damier. |
| SmallConfetti | `44` | Petits confettis. |
| SmallGrid | `45` | Petite grille. |
| SolidDiamond | `46` | Diamant massif. |
| Sphere | `47` | Sphère. |
| Trellis | `48` | Treillis. |
| UpwardDiagonal | `49` | Diagonale vers le haut. |
| Vertical | `50` | Verticale. |
| Wave | `51` | Vague. |
| Weave | `52` | Tisser. |
| WideDownwardDiagonal | `53` | Large diagonale vers le bas. |
| WideUpwardDiagonal | `54` | Large diagonale vers le haut. |
| ZigZag | `55` | Zigzag. |

## Exemples

Montre comment définir un motif pour une forme.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// Il existe plusieurs façons de spécifier le remplissage d'un motif.
// 1 - Appliquer le motif au remplissage de la forme :
fill.Patterned(PatternType.DiagonalBrick);

// 2 - Appliquer un motif avec des couleurs de premier plan et d'arrière-plan au remplissage de la forme :
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
