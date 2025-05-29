---
title: Stroke.Weight
linktitle: Weight
articleTitle: Weight
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Épaisseur du trait pour personnaliser l'épaisseur du pinceau pour les formes. Sublimez vos créations avec des tracés précis en points !
type: docs
weight: 260
url: /fr/net/aspose.words.drawing/stroke/weight/
---
## Stroke.Weight property

Définit l'épaisseur du pinceau qui parcourt le chemin d'une forme en points.

```csharp
public double Weight { get; set; }
```

## Remarques

La valeur par défaut pour un[`Shape`](../../shape/) est de 0,75.

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

* class [Stroke](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
