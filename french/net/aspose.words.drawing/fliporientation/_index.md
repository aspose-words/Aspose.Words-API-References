---
title: Enum FlipOrientation
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Drawing.FlipOrientation énumération. Valeurs possibles pour lorientation dune forme.
type: docs
weight: 970
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
| Horizontal | `1` | Retourner le long de l'axe y, en inversant les coordonnées x. |
| Vertical | `2` | Retourner le long de l'axe x, en inversant les coordonnées y. |
| Both | `3` | Retourner le long des axes y et x. |

### Exemples

Montre comment retourner une forme sur un axe.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère une forme d'image et laisse son orientation dans son état par défaut.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

Assert.AreEqual(FlipOrientation.None, shape.FlipOrientation);

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Définissez la propriété "FlipOrientation" sur "FlipOrientation.Horizontal" pour retourner la deuxième forme sur l'axe y,
// en faisant une image miroir horizontale de la première forme.
shape.FlipOrientation = FlipOrientation.Horizontal;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Définissez la propriété "FlipOrientation" sur "FlipOrientation.Horizontal" pour retourner la troisième forme sur l'axe des x,
// en faisant une image miroir verticale de la première forme.
shape.FlipOrientation = FlipOrientation.Vertical;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Définissez la propriété "FlipOrientation" sur "FlipOrientation.Horizontal" pour retourner la quatrième forme sur les axes x et y,
// en faisant une image miroir horizontale et verticale de la première forme.
shape.FlipOrientation = FlipOrientation.Both;

doc.Save(ArtifactsDir + "Shape.FlipShapeOrientation.docx");
```

### Voir également

* property [FlipOrientation](../shapebase/fliporientation/)
* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)


