---
title: Stroke.LineStyle
second_title: Référence de l'API Aspose.Words pour .NET
description: Stroke propriété. Définit le style de trait du trait.
type: docs
weight: 120
url: /fr/net/aspose.words.drawing/stroke/linestyle/
---
## Stroke.LineStyle property

Définit le style de trait du trait.

```csharp
public ShapeLineStyle LineStyle { get; set; }
```

### Remarques

La valeur par défaut estSingle.

### Exemples

Montre comment modifier les propriétés de trait.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// Les formes de base, telles que le rectangle, ont deux parties visibles.
// 1 - Le remplissage, qui s'applique à la zone à l'intérieur du contour de la forme :
shape.Fill.ForeColor = Color.White;

// 2 - Le trait, qui marque le contour de la forme :
// Modifie diverses propriétés du trait de cette forme.
Stroke stroke = shape.Stroke;
stroke.On = true;
stroke.Weight = 5;
stroke.Color = Color.Red;
stroke.DashStyle = DashStyle.ShortDashDotDot;
stroke.JoinStyle = JoinStyle.Miter;
stroke.EndCap = EndCap.Square;
stroke.LineStyle = ShapeLineStyle.Triple;

doc.Save(ArtifactsDir + "Shape.Stroke.docx");
```

### Voir également

* enum [ShapeLineStyle](../../shapelinestyle/)
* class [Stroke](../)
* espace de noms [Aspose.Words.Drawing](../../stroke/)
* Assemblée [Aspose.Words](../../../)


