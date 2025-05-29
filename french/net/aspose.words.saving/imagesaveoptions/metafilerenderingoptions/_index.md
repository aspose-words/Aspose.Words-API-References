---
title: ImageSaveOptions.MetafileRenderingOptions
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ImageSaveOptions MetafileRenderingOptions pour contrôler la gestion des métafichiers dans votre sortie rendue pour une qualité d'image améliorée.
type: docs
weight: 90
url: /fr/net/aspose.words.saving/imagesaveoptions/metafilerenderingoptions/
---
## ImageSaveOptions.MetafileRenderingOptions property

Permet de spécifier comment les métafichiers sont traités dans la sortie rendue.

```csharp
public MetafileRenderingOptions MetafileRenderingOptions { get; }
```

## Remarques

QuandVector est spécifié, Aspose.Words rend le métafichier en graphiques vectoriels en utilisant d'abord son propre moteur de rendu de métafichier, puis rend les graphiques vector en image.

QuandBitmap est spécifié, Aspose.Words rend le métafichier directement dans l'image à l'aide du moteur de rendu de métafichier GDI+.

Le moteur de rendu de métafichiers GDI+ est plus rapide et prend en charge la quasi-totalité des fonctionnalités des métafichiers. Cependant, en basse résolution, le rendu peut être incohérent par rapport aux autres graphiques vectoriels (notamment pour le texte) de la page. Le moteur de rendu de métafichiers Aspose.Words produit un résultat plus cohérent, même en basse résolution, mais il est plus lent et peut rendre les métafichiers complexes de manière inexacte.

La valeur par défaut pour[`MetafileRenderingMode`](../../metafilerenderingmode/) estBitmap.

## Exemples

Montre comment définir le mode de rendu lors de l'enregistrement de documents avec des images Windows Metafile dans d'autres formats d'image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Windows MetaFile.wmf");

// Lorsque nous enregistrons le document sous forme d'image, nous pouvons passer un objet SaveOptions à
// déterminer comment l'opération de sauvegarde traitera les métafichiers Windows dans le document.
// Si nous définissons la propriété "RenderingMode" sur "MetafileRenderingMode.Vector",
// ou "MetafileRenderingMode.VectorWithFallback", nous rendrons tous les métafichiers sous forme de graphiques vectoriels.
// Si nous définissons la propriété « RenderingMode » sur « MetafileRenderingMode.Bitmap », nous rendrons tous les métafichiers sous forme de bitmaps.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.MetafileRenderingOptions.RenderingMode = metafileRenderingMode;
// Aspose.Words utilise GDI+ pour l'émulation des opérations raster, lorsque la valeur est définie sur true.
options.MetafileRenderingOptions.UseGdiRasterOperationsEmulation = true;

doc.Save(ArtifactsDir + "ImageSaveOptions.WindowsMetaFile.png", options);
```

### Voir également

* class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* class [ImageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
