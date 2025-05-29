---
title: ShapeLineStyle Enum
linktitle: ShapeLineStyle
articleTitle: ShapeLineStyle
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Drawing.ShapeLineStyle pour améliorer la conception de votre document avec des styles de lignes composées personnalisables pour les formes.
type: docs
weight: 1660
url: /fr/net/aspose.words.drawing/shapelinestyle/
---
## ShapeLineStyle enumeration

Spécifie le style de ligne composé d'un[`Shape`](../shape/) .

```csharp
public enum ShapeLineStyle
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Single | `0` | Ligne unique. |
| Double | `1` | Lignes doubles de largeur égale. |
| ThickThin | `2` | Lignes doubles, une épaisse, une fine. |
| ThinThick | `3` | Lignes doubles, une fine, une épaisse. |
| Triple | `4` | Trois lignes, fine, épaisse, fine. |
| Default | `0` | La valeur par défaut estSingle . |

## Exemples

Montre comment modifier les propriétés du trait.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// Les formes de base, comme le rectangle, ont deux parties visibles.
// 1 - Le remplissage, qui s'applique à la zone à l'intérieur du contour de la forme :
shape.Fill.ForeColor = Color.White;

// 2 - Le trait, qui marque le contour de la forme :
// Modifier diverses propriétés du trait de cette forme.
Stroke stroke = shape.Stroke;
stroke.On = true;
stroke.Weight = 5;
stroke.Color = Color.Red;
stroke.DashStyle = DashStyle.ShortDashDotDot;
stroke.JoinStyle = JoinStyle.Miter;
stroke.EndCap = EndCap.Square;
stroke.LineStyle = ShapeLineStyle.Triple;
stroke.Fill.TwoColorGradient(Color.Red, Color.Blue, GradientStyle.Vertical, GradientVariant.Variant1);

doc.Save(ArtifactsDir + "Shape.Stroke.docx");
```

### Voir également

* property [LineStyle](../stroke/linestyle/)
* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
