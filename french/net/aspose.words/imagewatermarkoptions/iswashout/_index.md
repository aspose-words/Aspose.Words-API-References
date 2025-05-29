---
title: ImageWatermarkOptions.IsWashout
linktitle: IsWashout
articleTitle: IsWashout
second_title: Aspose.Words pour .NET
description: Découvrez la propriété IsWashout d'ImageWatermarkOptions. Contrôlez facilement l'effet de délavage de votre filigrane grâce à ce paramètre booléen simple.
type: docs
weight: 20
url: /fr/net/aspose.words/imagewatermarkoptions/iswashout/
---
## ImageWatermarkOptions.IsWashout property

Obtient ou définit une valeur booléenne qui est responsable de l'effet de délavage du filigrane. La valeur par défaut est`vrai` .

```csharp
public bool IsWashout { get; set; }
```

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
