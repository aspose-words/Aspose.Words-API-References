---
title: ImageColorMode Enum
linktitle: ImageColorMode
articleTitle: ImageColorMode
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Saving.ImageColorMode pour optimiser les images des pages de documents. Contrôlez les modes de couleur pour une qualité visuelle améliorée dans vos projets.
type: docs
weight: 5960
url: /fr/net/aspose.words.saving/imagecolormode/
---
## ImageColorMode enumeration

Spécifie le mode couleur pour les images générées des pages du document.

```csharp
public enum ImageColorMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Les pages du document seront rendues sous forme d'images couleur. |
| Grayscale | `1` | Les pages du document seront rendues sous forme d'images en niveaux de gris. |
| BlackAndWhite | `2` | Les pages du document seront rendues sous forme d'images en noir et blanc. |

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

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
