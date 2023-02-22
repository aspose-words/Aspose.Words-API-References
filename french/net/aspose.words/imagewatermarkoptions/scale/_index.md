---
title: ImageWatermarkOptions.Scale
second_title: Référence de l'API Aspose.Words pour .NET
description: ImageWatermarkOptions propriété. Obtient ou définit le facteur déchelle exprimé en fraction de limage. La valeur par défaut est 0  auto.
type: docs
weight: 30
url: /fr/net/aspose.words/imagewatermarkoptions/scale/
---
## ImageWatermarkOptions.Scale property

Obtient ou définit le facteur d'échelle exprimé en fraction de l'image. La valeur par défaut est 0 - auto.

```csharp
public double Scale { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Lance lorsque l'argument est en dehors de la plage de valeurs valides. |

### Remarques

Les valeurs valides sont comprises entre 0 et 65,5 inclus.

L'échelle automatique signifie que le filigrane sera mis à l'échelle à sa largeur maximale et sa hauteur maximale par rapport à les marges de la page.

### Exemples

Montre comment créer un filigrane à partir d'une image dans le système de fichiers local.

```csharp
Document doc = new Document();

            // Modifier l'apparence du filigrane de l'image avec un objet ImageWatermarkOptions,
            // puis passez-le lors de la création d'un filigrane à partir d'un fichier image.
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
* espace de noms [Aspose.Words](../../imagewatermarkoptions/)
* Assemblée [Aspose.Words](../../../)


