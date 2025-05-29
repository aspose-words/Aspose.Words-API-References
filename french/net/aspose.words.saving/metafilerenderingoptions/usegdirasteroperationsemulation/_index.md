---
title: MetafileRenderingOptions.UseGdiRasterOperationsEmulation
linktitle: UseGdiRasterOperationsEmulation
articleTitle: UseGdiRasterOperationsEmulation
second_title: Aspose.Words pour .NET
description: Découvrez la propriété UseGdiRasterOperationsEmulation de MetafileRenderingOptions pour optimiser les opérations raster avec GDI. Améliorez vos performances et votre flexibilité dès aujourd'hui !
type: docs
weight: 80
url: /fr/net/aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/
---
## MetafileRenderingOptions.UseGdiRasterOperationsEmulation property

Obtient ou définit une valeur déterminant s'il faut ou non utiliser GDI+ pour l'émulation des opérations raster.

```csharp
public bool UseGdiRasterOperationsEmulation { get; set; }
```

## Remarques

La bibliothèque Windows GDI+ peut être utilisée pour émuler les opérations raster. Elle prend en charge toutes les opérations raster (x000d_) par rapport à l'émulation Aspose.Words, mais les performances peuvent être plus lentes dans certains cas.

Lorsque cette valeur est définie sur`vrai`Aspose.Words utilise GDI+ pour l'émulation des opérations raster.

Lorsque cette valeur est définie sur`FAUX`Aspose.Words utilise sa propre implémentation de l'émulation des opérations raster.

Cette option est utilisée uniquement lorsque le métafichier est rendu sous forme de graphiques vectoriels.

La valeur par défaut est`FAUX`.

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

* class [MetafileRenderingOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
