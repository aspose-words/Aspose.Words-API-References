---
title: FixedPageSaveOptions.JpegQuality
second_title: Référence de l'API Aspose.Words pour .NET
description: FixedPageSaveOptions propriété. Obtient ou définit une valeur déterminant la qualité des images JPEG dans le document HTML.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/fixedpagesaveoptions/jpegquality/
---
## FixedPageSaveOptions.JpegQuality property

Obtient ou définit une valeur déterminant la qualité des images JPEG dans le document HTML.

```csharp
public int JpegQuality { get; set; }
```

### Remarques

N'a d'effet que lorsqu'un document contient des images JPEG.

Utilisez cette propriété pour obtenir ou définir la qualité des images à l'intérieur d'un document lors de l'enregistrement au format de page fixe. La valeur peut varier de 0 à 100, où 0 signifie la pire qualité mais une compression maximale et 100 signifie la meilleure qualité mais une compression minimale.

La valeur par défaut est 95.

### Exemples

Montre comment configurer la compression lors de l'enregistrement d'un document au format JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Crée un objet "ImageSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode rend le document en image.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// Définissez la propriété "JpegQuality" sur "10" pour utiliser une compression plus forte lors du rendu du document.
// Cela réduira la taille du fichier du document, mais l'image affichera des artefacts de compression plus importants.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// Définissez la propriété "JpegQuality" sur "100" pour utiliser une compression plus faible lors du rendu du document.
// Cela améliorera la qualité de l'image au prix d'une taille de fichier accrue.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

### Voir également

* class [FixedPageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../fixedpagesaveoptions/)
* Assemblée [Aspose.Words](../../../)


