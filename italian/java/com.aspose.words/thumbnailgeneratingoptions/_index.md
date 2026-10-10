---
title: "ThumbnailGeneratingOptions"
linktitle: "ThumbnailGeneratingOptions"
second_title: "Aspose.Words per Java"
description: "Può essere usato per specificare opzioni aggiuntive durante la generazione della miniatura per un documento in Java."
type: docs
weight: 687
url: /it/java/com.aspose.words/thumbnailgeneratingoptions/
---

**Inheritance:**
java.lang.Object
```
public class ThumbnailGeneratingOptions
```

Può essere usato per specificare opzioni aggiuntive durante la generazione di una miniatura per un documento.

 **Remarks:** 

L'utente può chiamare il metodo [Document.updateThumbnail(com.aspose.words.ThumbnailGeneratingOptions)](../../com.aspose.words/document/\#updateThumbnail-com.aspose.words.ThumbnailGeneratingOptions) per generare [BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties/\#getThumbnail) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties/\#setThumbnail-byte) per un documento.

 **Examples:** 

Mostra come aggiornare la miniatura di un documento.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getGenerateFromFirstPage()](#getGenerateFromFirstPage) | Specifica se generare la miniatura dalla prima pagina del documento o dalla prima immagine. |
| [getThumbnailSize()](#getThumbnailSize) | Dimensione della miniatura generata in pixel. |
| [setGenerateFromFirstPage(boolean value)](#setGenerateFromFirstPage-boolean) | Specifica se generare la miniatura dalla prima pagina del documento o dalla prima immagine. |
| [setThumbnailSize(Dimension value)](#setThumbnailSize-java.awt.Dimension) | Dimensione della miniatura generata in pixel. |
### getGenerateFromFirstPage() {#getGenerateFromFirstPage}
```
public boolean getGenerateFromFirstPage()
```


Specifica se generare la miniatura dalla prima pagina del documento o dalla prima immagine.

 **Remarks:** 

Il valore predefinito è  true , il che significa che la miniatura verrà generata dalla prima pagina del documento. Se il valore è  false  e non c'è alcuna immagine nel documento, la miniatura verrà generata dalla prima pagina del documento.

 **Examples:** 

Mostra come aggiornare la miniatura di un documento.

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
boolean - Il valore booleano corrispondente.
### getThumbnailSize() {#getThumbnailSize}
```
public Dimension getThumbnailSize()
```


Dimensione della miniatura generata in pixel. Il valore predefinito è 600x900.

 **Examples:** 

Mostra come aggiornare la miniatura di un documento.

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
java.awt.Dimension - Il valore corrispondente java.awt.Dimension.
### setGenerateFromFirstPage(boolean value) {#setGenerateFromFirstPage-boolean}
```
public void setGenerateFromFirstPage(boolean value)
```


Specifica se generare la miniatura dalla prima pagina del documento o dalla prima immagine.

 **Remarks:** 

Il valore predefinito è  true , il che significa che la miniatura verrà generata dalla prima pagina del documento. Se il valore è  false  e non c'è alcuna immagine nel documento, la miniatura verrà generata dalla prima pagina del documento.

 **Examples:** 

Mostra come aggiornare la miniatura di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setThumbnailSize(Dimension value) {#setThumbnailSize-java.awt.Dimension}
```
public void setThumbnailSize(Dimension value)
```


Dimensione della miniatura generata in pixel. Il valore predefinito è 600x900.

 **Examples:** 

Mostra come aggiornare la miniatura di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.awt.Dimension | Il valore corrispondente java.awt.Dimension. |

