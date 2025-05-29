---
title: ImageData.ImageSize
linktitle: ImageSize
articleTitle: ImageSize
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ImageData ImageSize pour accéder facilement aux détails essentiels sur les dimensions et la résolution de l'image pour une qualité visuelle améliorée.
type: docs
weight: 130
url: /fr/net/aspose.words.drawing/imagedata/imagesize/
---
## ImageData.ImageSize property

Obtient les informations sur la taille et la résolution de l'image.

```csharp
public ImageSize ImageSize { get; }
```

## Remarques

Si l'image est uniquement liée et non stockée dans le document, renvoie une taille zéro.

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

* class [ImageSize](../../imagesize/)
* class [ImageData](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
