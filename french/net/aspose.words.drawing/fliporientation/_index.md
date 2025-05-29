---
title: FlipOrientation Enum
linktitle: FlipOrientation
articleTitle: FlipOrientation
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Drawing.FlipOrientation pour des options d'orientation de formes polyvalentes. Améliorez la conception de vos documents grâce à une personnalisation flexible !
type: docs
weight: 1290
url: /fr/net/aspose.words.drawing/fliporientation/
---
## FlipOrientation enumeration

Valeurs possibles pour l'orientation d'une forme.

```csharp
[Flags]
public enum FlipOrientation
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Les coordonnées ne sont pas inversées. |
| Horizontal | `1` | Basculez le long de l'axe des y, en inversant les coordonnées x. |
| Vertical | `2` | Basculez le long de l'axe des x, en inversant les coordonnées y. |
| Both | `3` | Basculez le long des axes y et x. |

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

* property [FlipOrientation](../shapebase/fliporientation/)
* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
