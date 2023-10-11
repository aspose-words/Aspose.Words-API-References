---
title: Enum ImagePixelFormat
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.ImagePixelFormat énumération. Spécifie le format de pixel pour les images générées des pages du document.
type: docs
weight: 5220
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

### Exemples

Montre comment sélectionner un débit bit par pixel avec lequel restituer un document en image.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            Assert.That(20000, Is.LessThan(new FileInfo(ImageDir + "Logo.jpg").Length));

            // Lorsque nous enregistrons le document sous forme d'image, nous pouvons passer un objet SaveOptions à
            // sélectionne un format de pixel pour l'image que l'opération de sauvegarde générera.
            // Différents débits bit par pixel affecteront la qualité et la taille du fichier de l'image générée.
            ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
            imageSaveOptions.PixelFormat = imagePixelFormat;

            // Nous pouvons cloner les instances ImageSaveOptions.
            Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

            doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);

#if NET48 || JAVA
            switch (imagePixelFormat)
            {
                case ImagePixelFormat.Format1bppIndexed:
                    Assert.That(10000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format16BppRgb555:
                    Assert.That(80000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format24BppRgb:
                    Assert.That(125000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format32BppRgb:
                    Assert.That(150000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format48BppRgb:
                    Assert.That(200000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
            }
#elif NET5_0_OR_GREATER
            switch (imagePixelFormat)
            {
                case ImagePixelFormat.Format1bppIndexed:
                    Assert.That(10000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format24BppRgb:
                    Assert.That(70000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format16BppRgb555:
                case ImagePixelFormat.Format32BppRgb:
                case ImagePixelFormat.Format48BppRgb:
                    Assert.That(125000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
            }
#endif
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


