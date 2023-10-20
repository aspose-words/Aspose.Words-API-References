---
title: ThumbnailGeneratingOptions.GenerateFromFirstPage
linktitle: GenerateFromFirstPage
articleTitle: GenerateFromFirstPage
second_title: Aspose.Words pour .NET
description: ThumbnailGeneratingOptions GenerateFromFirstPage propriété. Spécifie sil faut générer une vignette à partir de la première page du document ou de la première image en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/
---
## ThumbnailGeneratingOptions.GenerateFromFirstPage property

Spécifie s'il faut générer une vignette à partir de la première page du document ou de la première image.

```csharp
public bool GenerateFromFirstPage { get; set; }
```

## Remarques

La valeur par défaut est`vrai` , ce qui signifie que la vignette sera générée à partir de la première page du document. Si la valeur est`FAUX` et il n'y a pas d'image dans le document, la vignette sera générée à partir de la première page du document.

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

// 2 - Utiliser la première image trouvée dans le document :
ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
options.ThumbnailSize = new Size(400, 400);
options.GenerateFromFirstPage = false;

doc.UpdateThumbnail(options);
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstImage.epub");
```

### Voir également

* class [ThumbnailGeneratingOptions](../)
* espace de noms [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Assemblée [Aspose.Words](../../../)
