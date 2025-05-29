---
title: ImageSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words pour .NET
description: Ajustez la propriété JpegQuality dans ImageSaveOptions pour optimiser la qualité des images JPEG et obtenir des visuels époustouflants et de meilleures performances. Idéal pour les développeurs !
type: docs
weight: 80
url: /fr/net/aspose.words.saving/imagesaveoptions/jpegquality/
---
## ImageSaveOptions.JpegQuality property

Obtient ou définit une valeur déterminant la qualité des images JPEG générées.

```csharp
public int JpegQuality { get; set; }
```

## Remarques

N'a d'effet que lors de l'enregistrement au format JPEG.

Utilisez cette propriété pour obtenir ou définir la qualité des images générées lors de l'enregistrement au format JPEG. La valeur peut varier de 0 à 100 où 0 signifie la pire qualité mais la compression maximale et 100 signifie la meilleure qualité mais la compression minimale.

La valeur par défaut est 95.

## Exemples

Montre comment configurer la compression lors de l'enregistrement d'un document au format JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Créez un objet « ImageSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode rend le document en image.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);
// Définissez la propriété « JpegQuality » sur « 10 » pour utiliser une compression plus forte lors du rendu du document.
// Cela réduira la taille du fichier du document, mais l'image affichera des artefacts de compression plus importants.
imageOptions.JpegQuality = 10;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Définissez la propriété « JpegQuality » sur « 100 » pour utiliser une compression plus faible lors du rendu du document.
// Cela améliorera la qualité de l'image au prix d'une augmentation de la taille du fichier.
imageOptions.JpegQuality = 100;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

### Voir également

* class [ImageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
