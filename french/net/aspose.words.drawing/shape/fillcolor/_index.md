---
title: Shape.FillColor
linktitle: FillColor
articleTitle: FillColor
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Shape FillColor pour personnaliser vos créations avec des couleurs de pinceau vibrantes qui améliorent vos formes et rehaussent vos projets.
type: docs
weight: 50
url: /fr/net/aspose.words.drawing/shape/fillcolor/
---
## Shape.FillColor property

Définit la couleur du pinceau qui remplit le tracé fermé de la forme.

```csharp
public Color FillColor { get; set; }
```

## Remarques

Il s'agit d'un raccourci vers le[`Color`](../../fill/color/) propriété.

La valeur par défaut est White .

## Exemples

Montre comment remplir une forme avec une couleur unie.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Écrivez du texte, puis recouvrez-le d'une forme flottante.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Utilisez la propriété « StrokeColor » pour définir la couleur du contour de la forme.
shape.StrokeColor = Color.CadetBlue;

// Utilisez la propriété « FillColor » pour définir la couleur de la zone intérieure de la forme.
shape.FillColor = Color.LightBlue;

// La propriété « Opacité » détermine le degré de transparence de la couleur sur une échelle de 0 à 1,
// avec 1 étant totalement opaque et 0 étant invisible.
// Le remplissage de la forme par défaut est entièrement opaque, nous ne pouvons donc pas voir le texte sur lequel se trouve cette forme.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Définissez l'opacité de la couleur de remplissage de la forme sur une valeur inférieure afin que nous puissions voir le texte en dessous.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Voir également

* class [Shape](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
