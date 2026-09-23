---
title: "ThumbnailGeneratingOptions"
linktitle: "ThumbnailGeneratingOptions"
second_title: "Aspose.Words pour Java"
description: "Peut être utilisé pour spécifier des options supplémentaires lors de la génération d'une miniature pour un document en Java."
type: docs
weight: 687
url: /fr/java/com.aspose.words/thumbnailgeneratingoptions/
---

**Inheritance:**
java.lang.Object
```
public class ThumbnailGeneratingOptions
```

Peut être utilisé pour spécifier des options supplémentaires lors de la génération d’une vignette pour un document.

 **Remarks:** 

L'utilisateur peut appeler la méthode [Document.updateThumbnail(com.aspose.words.ThumbnailGeneratingOptions)](../../com.aspose.words/document/\#updateThumbnail-com.aspose.words.ThumbnailGeneratingOptions) pour générer [BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties/\#getThumbnail) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties/\#setThumbnail-byte) pour un document.

 **Examples:** 

Montre comment mettre à jour la miniature d'un document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // There are two ways of setting a thumbnail image when saving a document to .epub.
 // 1 -  Use the document's first page:
 doc.updateThumbnail();
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstPage.epub");

 // 2 -  Use the first image found in the document:
 ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
 options.setThumbnailSize(new Dimension(400, 400));
 options.setGenerateFromFirstPage(false);

 doc.updateThumbnail(options);
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstImage.epub");
 
```
## Méthodes

| Méthode | Description |
| --- | --- |
| [getGenerateFromFirstPage()](#getGenerateFromFirstPage) | Spécifie s'il faut générer la miniature à partir de la première page du document ou de la première image. |
| [getThumbnailSize()](#getThumbnailSize) | Taille de la vignette générée en pixels. |
| [setGenerateFromFirstPage(boolean value)](#setGenerateFromFirstPage-boolean) | Spécifie s'il faut générer la miniature à partir de la première page du document ou de la première image. |
| [setThumbnailSize(Dimension value)](#setThumbnailSize-java.awt.Dimension) | Taille de la vignette générée en pixels. |
### getGenerateFromFirstPage() {#getGenerateFromFirstPage}
```
public boolean getGenerateFromFirstPage()
```


Spécifie s'il faut générer la miniature à partir de la première page du document ou de la première image.

 **Remarks:** 

Par défaut, c'est  true , ce qui signifie que la vignette sera générée à partir de la première page du document. Si la valeur est  false  et qu'il n'y a aucune image dans le document, la vignette sera générée à partir de la première page du document.

 **Examples:** 

Montre comment mettre à jour la miniature d'un document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // There are two ways of setting a thumbnail image when saving a document to .epub.
 // 1 -  Use the document's first page:
 doc.updateThumbnail();
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstPage.epub");

 // 2 -  Use the first image found in the document:
 ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
 options.setThumbnailSize(new Dimension(400, 400));
 options.setGenerateFromFirstPage(false);

 doc.updateThumbnail(options);
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstImage.epub");
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getThumbnailSize() {#getThumbnailSize}
```
public Dimension getThumbnailSize()
```


Taille de la vignette générée en pixels. Par défaut, 600x900.

 **Examples:** 

Montre comment mettre à jour la miniature d'un document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // There are two ways of setting a thumbnail image when saving a document to .epub.
 // 1 -  Use the document's first page:
 doc.updateThumbnail();
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstPage.epub");

 // 2 -  Use the first image found in the document:
 ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
 options.setThumbnailSize(new Dimension(400, 400));
 options.setGenerateFromFirstPage(false);

 doc.updateThumbnail(options);
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstImage.epub");
 
```

**Returns:**
java.awt.Dimension - La valeur java.awt.Dimension correspondante.
### setGenerateFromFirstPage(boolean value) {#setGenerateFromFirstPage-boolean}
```
public void setGenerateFromFirstPage(boolean value)
```


Spécifie s'il faut générer la miniature à partir de la première page du document ou de la première image.

 **Remarks:** 

Par défaut, c'est  true , ce qui signifie que la vignette sera générée à partir de la première page du document. Si la valeur est  false  et qu'il n'y a aucune image dans le document, la vignette sera générée à partir de la première page du document.

 **Examples:** 

Montre comment mettre à jour la miniature d'un document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // There are two ways of setting a thumbnail image when saving a document to .epub.
 // 1 -  Use the document's first page:
 doc.updateThumbnail();
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstPage.epub");

 // 2 -  Use the first image found in the document:
 ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
 options.setThumbnailSize(new Dimension(400, 400));
 options.setGenerateFromFirstPage(false);

 doc.updateThumbnail(options);
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstImage.epub");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setThumbnailSize(Dimension value) {#setThumbnailSize-java.awt.Dimension}
```
public void setThumbnailSize(Dimension value)
```


Taille de la vignette générée en pixels. Par défaut, 600x900.

 **Examples:** 

Montre comment mettre à jour la miniature d'un document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // There are two ways of setting a thumbnail image when saving a document to .epub.
 // 1 -  Use the document's first page:
 doc.updateThumbnail();
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstPage.epub");

 // 2 -  Use the first image found in the document:
 ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
 options.setThumbnailSize(new Dimension(400, 400));
 options.setGenerateFromFirstPage(false);

 doc.updateThumbnail(options);
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstImage.epub");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.awt.Dimension | La valeur java.awt.Dimension correspondante. |

