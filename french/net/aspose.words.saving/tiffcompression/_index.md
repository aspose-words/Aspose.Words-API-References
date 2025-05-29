---
title: TiffCompression Enum
linktitle: TiffCompression
articleTitle: TiffCompression
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.TiffCompression pour un enregistrement optimal des fichiers TIFF. Choisissez facilement le type de compression idéal pour des images de page de haute qualité.
type: docs
weight: 6430
url: /fr/net/aspose.words.saving/tiffcompression/
---
## TiffCompression enumeration

Spécifie le type de compression à appliquer lors de l'enregistrement des images de page dans un fichier TIFF.

```csharp
public enum TiffCompression
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Ne spécifie aucune compression. |
| Rle | `1` | Spécifie le schéma de compression RLE. |
| Lzw | `2` | Spécifie le schéma de compression LZW. En Java émulé par la compression Deflate (Zip). |
| Ccitt3 | `3` | Spécifie le schéma de compression CCITT3. |
| Ccitt4 | `4` | Spécifie le schéma de compression CCITT4. |

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

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
