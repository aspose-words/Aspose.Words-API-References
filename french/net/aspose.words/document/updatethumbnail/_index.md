---
title: Document.UpdateThumbnail
linktitle: UpdateThumbnail
articleTitle: UpdateThumbnail
second_title: Aspose.Words pour .NET
description: Mettez à jour facilement la miniature de votre document grâce à nos options personnalisables. Améliorez vos visuels et la présentation de vos documents dès aujourd'hui !
type: docs
weight: 840
url: /fr/net/aspose.words/document/updatethumbnail/
---
## UpdateThumbnail(*[ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)*) {#updatethumbnail_1}

Mises à jour[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) du document selon les options spécifiées.

```csharp
public void UpdateThumbnail(ThumbnailGeneratingOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| options | ThumbnailGeneratingOptions | Les options de génération à utiliser. |

## Remarques

Le[`ThumbnailGeneratingOptions`](../../../aspose.words.rendering/thumbnailgeneratingoptions/) vous permet de spécifier la source de la miniature, la taille et d'autres options. Si la tentative de génération de la miniature échoue, ne change pas.

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

* class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## UpdateThumbnail() {#updatethumbnail}

Mises à jour[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) du document en utilisant les options par défaut.

```csharp
public void UpdateThumbnail()
```

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

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
