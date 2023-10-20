---
title: ImageSaveOptions.MetafileRenderingOptions
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words pour .NET
description: ImageSaveOptions MetafileRenderingOptions propriété. Permet de spécifier comment les métafichiers sont traités dans la sortie rendue en C#.
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

QuandVector est spécifié, Aspose.Words rend d'abord le métafichier en graphiques vectoriels en utilisant son propre moteur de rendu de métafichier, puis restitue les graphiques vectoriels à l'image.

QuandBitmap est spécifié, Aspose.Words rend le métafichier directement dans l'image à l'aide du moteur de rendu du métafichier GDI+.

Le moteur de rendu des métafichiers GDI+ fonctionne plus rapidement, prend en charge presque toutes les fonctionnalités des métafichiers, mais sur les résolutions low , il peut produire des résultats incohérents par rapport au reste des graphiques vectoriels (en particulier pour le texte) sur la page. Le moteur de rendu de métafichiers Aspose.Words produira un résultat plus cohérent, même , sur les basses résolutions, mais fonctionnera plus lentement et pourra rendre des métafichiers complexes de manière inexacte.

La valeur par défaut pour[`MetafileRenderingMode`](../../metafilerenderingmode/) estBitmap.

## Exemples

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

* class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* class [ImageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
