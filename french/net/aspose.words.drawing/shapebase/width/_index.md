---
title: ShapeBase.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Largeur de la base de forme. Ajustez facilement la largeur du bloc contenant votre forme pour une flexibilité et une précision de conception accrues.
type: docs
weight: 610
url: /fr/net/aspose.words.drawing/shapebase/width/
---
## ShapeBase.Width property

Obtient ou définit la largeur du bloc contenant la forme.

```csharp
public double Width { get; set; }
```

## Remarques

Pour une forme de niveau supérieur, la valeur est en points.

Pour les formes d'un groupe, la valeur est dans l'espace de coordonnées et les unités du groupe parent.

La valeur par défaut est 0.

## Exemples

Montre comment insérer une image flottante et spécifier sa position et sa taille.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Configurez la propriété « RelativeHorizontalPosition » de la forme pour traiter la valeur de la propriété « Left »
 // comme la distance horizontale de la forme, en points, à partir du côté gauche de la page.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Définissez la distance horizontale de la forme par rapport au côté gauche de la page sur 100.
shape.Left = 100;

// Utilisez la propriété « RelativeVerticalPosition » de manière similaire pour positionner la forme 80 pt sous le haut de la page.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Définissez la hauteur de la forme, ce qui mettra automatiquement à l'échelle la largeur pour préserver les dimensions.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// Les propriétés « Bottom » et « Right » contiennent les bords inférieur et droit de l'image.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

Montre comment redimensionner une forme avec une image.

```csharp
// Lorsque nous insérons une image à l'aide de la méthode « InsertImage », le générateur met à l'échelle la forme qui affiche l'image de sorte que,
// lorsque nous visualisons le document en utilisant un zoom à 100 % dans Microsoft Word, la forme affiche l'image dans sa taille réelle.
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Une image 400x400 créera un objet ImageData avec une taille d'image de 300x300pt.
ImageSize imageSize = shape.ImageData.ImageSize;

Assert.AreEqual(300.0d, imageSize.WidthPoints);
Assert.AreEqual(300.0d, imageSize.HeightPoints);

// Si les dimensions d'une forme correspondent aux dimensions des données de l'image,
// alors la forme affiche l'image dans sa taille d'origine.
Assert.AreEqual(300.0d, shape.Width);
Assert.AreEqual(300.0d, shape.Height);

 // Réduisez la taille globale de la forme de 50 %.
shape.Width *= 0.5;

 // Les facteurs d'échelle s'appliquent à la fois à la largeur et à la hauteur pour préserver les proportions de la forme.
Assert.AreEqual(150.0d, shape.Width);
Assert.AreEqual(150.0d, shape.Height);

// Lorsque nous redimensionnons la forme, la taille des données de l'image reste la même.
Assert.AreEqual(300.0d, imageSize.WidthPoints);
Assert.AreEqual(300.0d, imageSize.HeightPoints);

// Nous pouvons référencer les dimensions des données d'image pour appliquer une mise à l'échelle basée sur la taille de l'image.
shape.Width = imageSize.WidthPoints * 1.1;

Assert.AreEqual(330.0d, shape.Width);
Assert.AreEqual(330.0d, shape.Height);

doc.Save(ArtifactsDir + "Image.ScaleImage.docx");
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
