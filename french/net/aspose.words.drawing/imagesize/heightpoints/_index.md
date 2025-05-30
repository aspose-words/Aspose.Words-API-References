---
title: ImageSize.HeightPoints
linktitle: HeightPoints
articleTitle: HeightPoints
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ImageSize HeightPoints pour récupérer facilement la hauteur d'une image en points  1 point équivaut à 1/72 pouce. Optimisez vos images sans effort !
type: docs
weight: 30
url: /fr/net/aspose.words.drawing/imagesize/heightpoints/
---
## ImageSize.HeightPoints property

Récupère la hauteur de l'image en points. 1 point correspond à 1/72 pouce.

```csharp
public double HeightPoints { get; }
```

## Exemples

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

* class [ImageSize](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
