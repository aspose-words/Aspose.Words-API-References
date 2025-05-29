---
title: ImagePixelFormat Enum
linktitle: ImagePixelFormat
articleTitle: ImagePixelFormat
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Saving.ImagePixelFormat pour optimiser le format des pixels des images de vos pages. Améliorez l'aspect visuel de vos documents sans effort !
type: docs
weight: 5970
url: /fr/net/aspose.words.saving/imagepixelformat/
---
## ImagePixelFormat enumeration

Spécifie le format de pixel pour les images générées des pages du document.

```csharp
public enum ImagePixelFormat
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Format16BppRgb555 | `0` | 16 bits par pixel, RVB. |
| Format16BppRgb565 | `1` | 16 bits par pixel, RVB. |
| Format16BppArgb1555 | `2` | 16 bits par pixel, ARGB. |
| Format24BppRgb | `3` | 24 bits par pixel, RVB. |
| Format32BppRgb | `4` | 32 bits par pixel, RVB. |
| Format32BppArgb | `5` | 32 bits par pixel, ARGB. |
| Format32BppPArgb | `6` | 32 bits par pixel, ARGB, alpha prémultiplié. |
| Format48BppRgb | `7` | 48 bits par pixel, RVB. |
| Format64BppArgb | `8` | 64 bits par pixel, ARGB. |
| Format64BppPArgb | `9` | 64 bits par pixel, ARGB, alpha prémultiplié. |
| Format1bppIndexed | `10` | 1 bit par pixel, indexé. |

## Exemples

Montre comment sélectionner un débit de bits par pixel avec lequel restituer un document en image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Lorsque nous enregistrons le document sous forme d'image, nous pouvons passer un objet SaveOptions à
// sélectionnez un format de pixel pour l'image que l'opération de sauvegarde générera.
// Différents débits de bits par pixel affecteront la qualité et la taille du fichier de l'image générée.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PixelFormat = imagePixelFormat;

// Nous pouvons cloner des instances ImageSaveOptions.
Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
