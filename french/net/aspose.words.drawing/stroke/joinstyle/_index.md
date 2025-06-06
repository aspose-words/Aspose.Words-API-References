---
title: Stroke.JoinStyle
linktitle: JoinStyle
articleTitle: JoinStyle
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Stroke JoinStyle pour améliorer vos polylignes avec des styles de jointure personnalisables pour des graphiques plus fluides et une flexibilité de conception améliorée.
type: docs
weight: 170
url: /fr/net/aspose.words.drawing/stroke/joinstyle/
---
## Stroke.JoinStyle property

Définit le style de jointure d'une polyligne.

```csharp
public JoinStyle JoinStyle { get; set; }
```

## Remarques

La valeur par défaut estRound.

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

* enum [JoinStyle](../../joinstyle/)
* class [Stroke](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
