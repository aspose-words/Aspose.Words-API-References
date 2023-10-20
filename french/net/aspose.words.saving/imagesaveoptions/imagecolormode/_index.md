---
title: ImageSaveOptions.ImageColorMode
linktitle: ImageColorMode
articleTitle: ImageColorMode
second_title: Aspose.Words pour .NET
description: ImageSaveOptions ImageColorMode propriété. Obtient ou définit le mode de couleur pour les images générées en C#.
type: docs
weight: 50
url: /fr/net/aspose.words.saving/imagesaveoptions/imagecolormode/
---
## ImageSaveOptions.ImageColorMode property

Obtient ou définit le mode de couleur pour les images générées.

```csharp
public ImageColorMode ImageColorMode { get; set; }
```

## Remarques

Cette propriété n'a d'effet que lors de l'enregistrement au format d'image raster.

La valeur par défaut estNone.

## Exemples

Montre comment définir un mode couleur lors du rendu des documents.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            Assert.That(20000, Is.LessThan(new FileInfo(ImageDir + "Logo.jpg").Length));

            // Lorsque nous enregistrons le document sous forme d'image, nous pouvons passer un objet SaveOptions à
            // sélectionne un mode de couleur pour l'image que l'opération de sauvegarde générera.
            // Si on fixe la propriété "ImageColorMode" à "ImageColorMode.BlackAndWhite",
            // l'opération de sauvegarde appliquera une réduction des couleurs en niveaux de gris lors du rendu du document.
            // Si on fixe la propriété "ImageColorMode" à "ImageColorMode.Grayscale",
            // l'opération de sauvegarde rendra le document dans une image monochrome.
            // Si nous définissons la propriété "ImageColorMode" sur "Aucun", l'opération de sauvegarde appliquera la méthode par défaut
            // et préserve toutes les couleurs du document dans l'image de sortie.
            ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
            imageSaveOptions.ImageColorMode = imageColorMode;

            doc.Save(ArtifactsDir + "ImageSaveOptions.ColorMode.png", imageSaveOptions);

#if NET48 || JAVA
            switch (imageColorMode)
            {
                case ImageColorMode.None:
                    Assert.That(150000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.Grayscale:
                    Assert.That(80000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.BlackAndWhite:
                    Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
            }
#elif NET5_0_OR_GREATER
            switch (imageColorMode)
            {
                case ImageColorMode.None:
                    Assert.That(120000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.Grayscale:
                    Assert.That(80000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.BlackAndWhite:
                    Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
            }
#endif
```

### Voir également

* enum [ImageColorMode](../../imagecolormode/)
* class [ImageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
