---
title: ImageSize Class
linktitle: ImageSize
articleTitle: ImageSize
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Drawing.ImageSize, votre ressource de référence pour des informations détaillées sur la taille et la résolution des images pour une qualité de document améliorée.
type: docs
weight: 1400
url: /fr/net/aspose.words.drawing/imagesize/
---
## ImageSize class

Contient des informations sur la taille et la résolution de l'image.

Pour en savoir plus, visitez le[Travailler avec des images](https://docs.aspose.com/words/net/working-with-images/) article de documentation.

```csharp
public class ImageSize
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [ImageSize](imagesize/#constructor)(*int, int*) | Initialise la largeur et la hauteur aux valeurs données en pixels. Initialise la résolution à 96 ppp. |
| [ImageSize](imagesize/#constructor_1)(*int, int, double, double*) | Initialise la largeur, la hauteur et la résolution aux valeurs données. |

## Propriétés

| Nom | La description |
| --- | --- |
| [HeightPixels](../../aspose.words.drawing/imagesize/heightpixels/) { get; } | Obtient la hauteur de l'image en pixels. |
| [HeightPoints](../../aspose.words.drawing/imagesize/heightpoints/) { get; } | Récupère la hauteur de l'image en points. 1 point correspond à 1/72 pouce. |
| [HorizontalResolution](../../aspose.words.drawing/imagesize/horizontalresolution/) { get; } | Obtient la résolution horizontale en DPI. |
| [VerticalResolution](../../aspose.words.drawing/imagesize/verticalresolution/) { get; } | Obtient la résolution verticale en DPI. |
| [WidthPixels](../../aspose.words.drawing/imagesize/widthpixels/) { get; } | Obtient la largeur de l'image en pixels. |
| [WidthPoints](../../aspose.words.drawing/imagesize/widthpoints/) { get; } | Obtient la largeur de l'image en points. 1 point correspond à 1/72 pouce. |

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

* property [ImageSize](../imagedata/imagesize/)
* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
