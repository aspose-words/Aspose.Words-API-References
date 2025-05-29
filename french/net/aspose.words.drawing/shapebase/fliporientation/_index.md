---
title: ShapeBase.FlipOrientation
linktitle: FlipOrientation
articleTitle: FlipOrientation
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShapeBase FlipOrientation pour changer sans effort l'orientation de votre forme, améliorant ainsi vos conceptions avec facilité et créativité.
type: docs
weight: 180
url: /fr/net/aspose.words.drawing/shapebase/fliporientation/
---
## ShapeBase.FlipOrientation property

Change l'orientation d'une forme.

```csharp
public FlipOrientation FlipOrientation { get; set; }
```

## Remarques

La valeur par défaut estNone.

## Exemples

Montre comment retourner une forme sur un axe.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez une forme d'image et laissez son orientation dans son état par défaut.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

Assert.AreEqual(FlipOrientation.None, shape.FlipOrientation);

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Définissez la propriété « FlipOrientation » sur « FlipOrientation.Horizontal » pour retourner la deuxième forme sur l'axe des y,
// en le transformant en une image miroir horizontale de la première forme.
shape.FlipOrientation = FlipOrientation.Horizontal;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Définissez la propriété « FlipOrientation » sur « FlipOrientation.Horizontal » pour retourner la troisième forme sur l'axe des x,
// en le transformant en une image miroir verticale de la première forme.
shape.FlipOrientation = FlipOrientation.Vertical;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Définissez la propriété « FlipOrientation » sur « FlipOrientation.Horizontal » pour retourner la quatrième forme sur les axes x et y,
// en le transformant en une image miroir horizontale et verticale de la première forme.
shape.FlipOrientation = FlipOrientation.Both;

doc.Save(ArtifactsDir + "Shape.FlipShapeOrientation.docx");
```

### Voir également

* enum [FlipOrientation](../../fliporientation/)
* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
