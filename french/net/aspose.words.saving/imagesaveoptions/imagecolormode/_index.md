---
title: ImageSaveOptions.ImageColorMode
linktitle: ImageColorMode
articleTitle: ImageColorMode
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ImageColorMode d'ImageSaveOptions pour personnaliser et optimiser facilement le mode couleur de vos images générées. Améliorez vos visuels dès aujourd'hui !
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

Cette propriété n'a d'effet que lors de l'enregistrement dans des formats d'image raster.

La valeur par défaut estNone.

## Exemples

Montre comment définir un mode couleur lors du rendu des documents.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Lorsque nous enregistrons le document sous forme d'image, nous pouvons passer un objet SaveOptions à
// sélectionnez un mode de couleur pour l'image que l'opération de sauvegarde va générer.
// Si nous définissons la propriété "ImageColorMode" sur "ImageColorMode.BlackAndWhite",
// l'opération de sauvegarde appliquera une réduction des couleurs en niveaux de gris lors du rendu du document.
 // Si nous définissons la propriété "ImageColorMode" sur "ImageColorMode.Grayscale",
// l'opération de sauvegarde rendra le document en une image monochrome.
// Si nous définissons la propriété « ImageColorMode » sur « None », l'opération de sauvegarde appliquera la méthode par défaut
// et conserver toutes les couleurs du document dans l'image de sortie.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.ImageColorMode = imageColorMode;

doc.Save(ArtifactsDir + "ImageSaveOptions.ColorMode.png", imageSaveOptions);
```

### Voir également

* enum [ImageColorMode](../../imagecolormode/)
* class [ImageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
