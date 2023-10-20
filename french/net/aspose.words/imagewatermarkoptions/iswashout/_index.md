---
title: ImageWatermarkOptions.IsWashout
linktitle: IsWashout
articleTitle: IsWashout
second_title: Aspose.Words pour .NET
description: ImageWatermarkOptions IsWashout propriété. Obtient ou définit une valeur booléenne responsable de leffet de délavage du filigrane. La valeur par défaut estvrai  en C#.
type: docs
weight: 20
url: /fr/net/aspose.words/imagewatermarkoptions/iswashout/
---
## ImageWatermarkOptions.IsWashout property

Obtient ou définit une valeur booléenne responsable de l'effet de délavage du filigrane. La valeur par défaut est`vrai` .

```csharp
public bool IsWashout { get; set; }
```

## Exemples

Montre comment créer un filigrane à partir d’une image dans le système de fichiers local.

```csharp
Document doc = new Document();

            // Modifier l'apparence du filigrane de l'image avec un objet ImageWatermarkOptions,
            // puis transmettez-le en créant un filigrane à partir d'un fichier image.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET48 || JAVA
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);
#elif NET5_0_OR_GREATER || __MOBILE__
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
