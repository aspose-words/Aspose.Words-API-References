---
title: ImageWatermarkOptions.Scale
linktitle: Scale
articleTitle: Scale
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Échelle d'ImageWatermarkOptions pour ajuster facilement la mise à l'échelle de l'image et optimiser le filigrane. La valeur par défaut est 0 auto pour une intégration transparente.
type: docs
weight: 30
url: /fr/net/aspose.words/imagewatermarkoptions/scale/
---
## ImageWatermarkOptions.Scale property

Récupère ou définit le facteur d'échelle, exprimé en fraction de l'image. La valeur par défaut est 0 (automatique).

```csharp
public double Scale { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Lancé lorsque l'argument est hors de la plage de valeurs valides. |

## Remarques

Les valeurs valides vont de 0 à 65,5 inclus.

La mise à l'échelle automatique signifie que le filigrane sera mis à l'échelle à sa largeur maximale et à sa hauteur maximale par rapport aux marges de la page.

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

* class [ImageWatermarkOptions](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
