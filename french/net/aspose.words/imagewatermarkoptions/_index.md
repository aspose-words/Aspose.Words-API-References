---
title: ImageWatermarkOptions Class
linktitle: ImageWatermarkOptions
articleTitle: ImageWatermarkOptions
second_title: Aspose.Words pour .NET
description: Découvrez Aspose.Words.ImageWatermarkOptions. Personnalisez facilement vos filigranes d'image grâce à des options polyvalentes pour une présentation optimisée de vos documents.
type: docs
weight: 3670
url: /fr/net/aspose.words/imagewatermarkoptions/
---
## ImageWatermarkOptions class

Contient des options qui peuvent être spécifiées lors de l'ajout d'un filigrane avec une image.

Pour en savoir plus, visitez le[Travailler avec le filigrane](https://docs.aspose.com/words/net/working-with-watermark/) article de documentation.

```csharp
public class ImageWatermarkOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [ImageWatermarkOptions](imagewatermarkoptions/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [IsWashout](../../aspose.words/imagewatermarkoptions/iswashout/) { get; set; } | Obtient ou définit une valeur booléenne qui est responsable de l'effet de délavage du filigrane. La valeur par défaut est`vrai` . |
| [Scale](../../aspose.words/imagewatermarkoptions/scale/) { get; set; } | Récupère ou définit le facteur d'échelle, exprimé en fraction de l'image. La valeur par défaut est 0 (automatique). |

## Exemples

Montre comment créer un filigrane à partir d'une image dans le système de fichiers local.

```csharp
Document doc = new Document();

            // Modifiez l'apparence du filigrane de l'image avec un objet ImageWatermarkOptions,
            // puis transmettez-le lors de la création d'un filigrane à partir d'un fichier image.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // Nous avons différentes options pour insérer une image :
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
