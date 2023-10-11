---
title: MetafileRenderingOptions.UseGdiRasterOperationsEmulation
second_title: Référence de l'API Aspose.Words pour .NET
description: MetafileRenderingOptions propriété. Obtient ou définit une valeur déterminant sil faut ou non utiliser GDI pour lémulation des opérations raster.
type: docs
weight: 80
url: /fr/net/aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/
---
## MetafileRenderingOptions.UseGdiRasterOperationsEmulation property

Obtient ou définit une valeur déterminant s'il faut ou non utiliser GDI+ pour l'émulation des opérations raster.

```csharp
public bool UseGdiRasterOperationsEmulation { get; set; }
```

### Remarques

La bibliothèque Windows GDI+ pourrait être utilisée pour émuler les opérations raster. Il prend en charge tous les raster operation par rapport à la propre émulation d'Aspose.Words, mais les performances peuvent être plus lentes dans certains cas.

Lorsque cette valeur est fixée à`vrai`, Aspose.Words utilise GDI+ pour l'émulation des opérations raster.

Lorsque cette valeur est fixée à`FAUX`, Aspose.Words utilise sa propre implémentation d'émulation d'opérations raster.

Cette option est utilisée uniquement lorsque le métafichier est rendu sous forme de graphiques vectoriels.

La valeur par défaut est`FAUX`.

### Exemples

Montre comment définir le mode de rendu lors de l’enregistrement de documents contenant des images de métafichier Windows dans d’autres formats d’image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(Image.FromFile(ImageDir + "Windows MetaFile.wmf"));

// Lorsque nous enregistrons le document sous forme d'image, nous pouvons passer un objet SaveOptions à
// détermine comment l'opération de sauvegarde traitera les métafichiers Windows dans le document.
// Si nous définissons la propriété "RenderingMode" sur "MetafileRenderingMode.Vector",
// ou "MetafileRenderingMode.VectorWithFallback", nous rendrons tous les métafichiers sous forme de graphiques vectoriels.
// Si nous définissons la propriété "RenderingMode" sur "MetafileRenderingMode.Bitmap", nous rendrons tous les métafichiers sous forme de bitmaps.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.MetafileRenderingOptions.RenderingMode = metafileRenderingMode;
// Aspose.Words utilise GDI+ pour l'émulation des opérations raster, lorsque la valeur est définie sur true.
options.MetafileRenderingOptions.UseGdiRasterOperationsEmulation = true;

doc.Save(ArtifactsDir + "ImageSaveOptions.WindowsMetaFile.png", options);
```

### Voir également

* class [MetafileRenderingOptions](../)
* espace de noms [Aspose.Words.Saving](../../metafilerenderingoptions/)
* Assemblée [Aspose.Words](../../../)


