---
title: ThumbnailGeneratingOptions Class
linktitle: ThumbnailGeneratingOptions
articleTitle: ThumbnailGeneratingOptions
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Rendering.ThumbnailGeneratingOptions pour améliorer la génération de vignettes de vos documents avec des fonctionnalités personnalisables et une qualité améliorée.
type: docs
weight: 5330
url: /fr/net/aspose.words.rendering/thumbnailgeneratingoptions/
---
## ThumbnailGeneratingOptions class

Peut être utilisé pour spécifier des options supplémentaires lors de la génération d'une vignette pour un document.

```csharp
public class ThumbnailGeneratingOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [ThumbnailGeneratingOptions](thumbnailgeneratingoptions/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [GenerateFromFirstPage](../../aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/) { get; set; } | Spécifie s'il faut générer la miniature à partir de la première page du document ou de la première image. |
| [ThumbnailSize](../../aspose.words.rendering/thumbnailgeneratingoptions/thumbnailsize/) { get; set; } | Taille de la vignette générée en pixels. La valeur par défaut est 600x900. |

## Remarques

L'utilisateur peut appeler la méthode[`UpdateThumbnail`](../../aspose.words/document/updatethumbnail/) pour générer [`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) pour un document.

## Exemples

Montre comment mettre à jour la miniature d'un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Il existe deux manières de définir une image miniature lors de l'enregistrement d'un document au format .epub.
// 1 - Utiliser la première page du document :
doc.UpdateThumbnail();
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstPage.epub");

// 2 - Utiliser la première image trouvée dans le document :
ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
options.ThumbnailSize = new Size(400, 400);
options.GenerateFromFirstPage = false;

doc.UpdateThumbnail(options);
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstImage.epub");
```

### Voir également

* espace de noms [Aspose.Words.Rendering](../../aspose.words.rendering/)
* Assemblée [Aspose.Words](../../)
