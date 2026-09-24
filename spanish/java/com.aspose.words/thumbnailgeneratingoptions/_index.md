---
title: "ThumbnailGeneratingOptions"
linktitle: "ThumbnailGeneratingOptions"
second_title: "Aspose.Words para Java"
description: "Puede usarse para especificar opciones adicionales al generar una miniatura para un documento en Java."
type: docs
weight: 687
url: /es/java/com.aspose.words/thumbnailgeneratingoptions/
---

**Inheritance:**
java.lang.Object
```
public class ThumbnailGeneratingOptions
```

Puede usarse para especificar opciones adicionales al generar una miniatura para un documento.

 **Remarks:** 

El usuario puede llamar al método [Document.updateThumbnail(com.aspose.words.ThumbnailGeneratingOptions)](../../com.aspose.words/document/\#updateThumbnail-com.aspose.words.ThumbnailGeneratingOptions) para generar [BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties/\#getThumbnail) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties/\#setThumbnail-byte) para un documento.

 **Examples:** 

Muestra cómo actualizar la miniatura de un documento.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getGenerateFromFirstPage()](#getGenerateFromFirstPage) | Especifica si generar la miniatura a partir de la primera página del documento o de la primera imagen. |
| [getThumbnailSize()](#getThumbnailSize) | Tamaño de la miniatura generada en píxeles. |
| [setGenerateFromFirstPage(boolean value)](#setGenerateFromFirstPage-boolean) | Especifica si generar la miniatura a partir de la primera página del documento o de la primera imagen. |
| [setThumbnailSize(Dimension value)](#setThumbnailSize-java.awt.Dimension) | Tamaño de la miniatura generada en píxeles. |
### getGenerateFromFirstPage() {#getGenerateFromFirstPage}
```
public boolean getGenerateFromFirstPage()
```


Especifica si generar la miniatura a partir de la primera página del documento o de la primera imagen.

 **Remarks:** 

El valor predeterminado es  true , lo que significa que la miniatura se generará a partir de la primera página del documento. Si el valor es  false  y no hay imagen en el documento, la miniatura se generará a partir de la primera página del documento.

 **Examples:** 

Muestra cómo actualizar la miniatura de un documento.

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
boolean - El valor  boolean  correspondiente.
### getThumbnailSize() {#getThumbnailSize}
```
public Dimension getThumbnailSize()
```


Tamaño de la miniatura generada en píxeles. El valor predeterminado es 600x900.

 **Examples:** 

Muestra cómo actualizar la miniatura de un documento.

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
java.awt.Dimension - El valor correspondiente de java.awt.Dimension.
### setGenerateFromFirstPage(boolean value) {#setGenerateFromFirstPage-boolean}
```
public void setGenerateFromFirstPage(boolean value)
```


Especifica si generar la miniatura a partir de la primera página del documento o de la primera imagen.

 **Remarks:** 

El valor predeterminado es  true , lo que significa que la miniatura se generará a partir de la primera página del documento. Si el valor es  false  y no hay imagen en el documento, la miniatura se generará a partir de la primera página del documento.

 **Examples:** 

Muestra cómo actualizar la miniatura de un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setThumbnailSize(Dimension value) {#setThumbnailSize-java.awt.Dimension}
```
public void setThumbnailSize(Dimension value)
```


Tamaño de la miniatura generada en píxeles. El valor predeterminado es 600x900.

 **Examples:** 

Muestra cómo actualizar la miniatura de un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.awt.Dimension | El valor correspondiente de java.awt.Dimension. |

