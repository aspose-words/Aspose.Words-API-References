---
title: ImageSaveOptions.TiffCompression
linktitle: TiffCompression
articleTitle: TiffCompression
second_title: Aspose.Words pour .NET
description: Optimisez vos images TIFF avec la propriété ImageSaveOptions TiffCompression, vous permettant de choisir la meilleure méthode de compression pour des résultats de qualité.
type: docs
weight: 180
url: /fr/net/aspose.words.saving/imagesaveoptions/tiffcompression/
---
## ImageSaveOptions.TiffCompression property

Obtient ou définit le type de compression à appliquer lors de l'enregistrement des images générées au format TIFF.

```csharp
public TiffCompression TiffCompression { get; set; }
```

## Remarques

N'a d'effet que lors de l'enregistrement au format TIFF.

La valeur par défaut estLzw.

## Exemples

Montre comment sélectionner le schéma de compression à appliquer à un document que nous convertissons en image TIFF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Logo.jpg");

// Créez un objet « ImageSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode rend le document en image.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
// Définissez la propriété « TiffCompression » sur « TiffCompression.None » pour n'appliquer aucune compression lors de l'enregistrement,
// ce qui peut donner lieu à un fichier de sortie très volumineux.
// Définissez la propriété « TiffCompression » sur « TiffCompression.Rle » pour appliquer la compression RLE
// Définissez la propriété « TiffCompression » sur « TiffCompression.Lzw » pour appliquer la compression LZW.
// Définissez la propriété « TiffCompression » sur « TiffCompression.Ccitt3 » pour appliquer la compression CCITT3.
// Définissez la propriété « TiffCompression » sur « TiffCompression.Ccitt4 » pour appliquer la compression CCITT4.
options.TiffCompression = tiffCompression;

doc.Save(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff", options);
```

### Voir également

* enum [TiffCompression](../../tiffcompression/)
* class [ImageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
