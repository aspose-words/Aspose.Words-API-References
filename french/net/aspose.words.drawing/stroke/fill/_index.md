---
title: Stroke.Fill
second_title: Référence de l'API Aspose.Words pour .NET
description: Stroke propriété. Obtient le formatage de remplissage pour leStroke .
type: docs
weight: 100
url: /fr/net/aspose.words.drawing/stroke/fill/
---
## Stroke.Fill property

Obtient le formatage de remplissage pour le[`Stroke`](../) .

```csharp
public Fill Fill { get; }
```

### Exemples

Montre comment modifier les propriétés du trait.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// Les formes de base, comme le rectangle, comportent deux parties visibles.
// 1 - Le remplissage, qui s'applique à la zone située à l'intérieur du contour de la forme :
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

* class [Fill](../../fill/)
* class [Stroke](../)
* espace de noms [Aspose.Words.Drawing](../../stroke/)
* Assemblée [Aspose.Words](../../../)


