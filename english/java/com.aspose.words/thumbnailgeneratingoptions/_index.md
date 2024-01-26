---
title: ThumbnailGeneratingOptions
linktitle: ThumbnailGeneratingOptions
second_title: Aspose.Words for Java
description: Can be used to specify additional options when generating thumbnail for a document in Java.
type: docs
weight: 615
url: /java/com.aspose.words/thumbnailgeneratingoptions/
---

**Inheritance:**
java.lang.Object
```
public class ThumbnailGeneratingOptions
```

Can be used to specify additional options when generating thumbnail for a document.

 **Remarks:** 

User can call method [Document.updateThumbnail(com.aspose.words.ThumbnailGeneratingOptions)](../../com.aspose.words/document/\#updateThumbnail-com.aspose.words.ThumbnailGeneratingOptions) to generate [BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties/\#getThumbnail) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties/\#setThumbnail-byte) for a document.

 **Examples:** 

Shows how to update a document's thumbnail.

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
## Methods

| Method | Description |
| --- | --- |
| [getGenerateFromFirstPage()](#getGenerateFromFirstPage) | Specifies whether to generate thumbnail from first page of the document or first image. |
| [getThumbnailSize()](#getThumbnailSize) | Size of generated thumbnail in pixels. |
| [setGenerateFromFirstPage(boolean value)](#setGenerateFromFirstPage-boolean) | Specifies whether to generate thumbnail from first page of the document or first image. |
| [setThumbnailSize(Dimension value)](#setThumbnailSize-java.awt.Dimension) | Size of generated thumbnail in pixels. |
### getGenerateFromFirstPage() {#getGenerateFromFirstPage}
```
public boolean getGenerateFromFirstPage()
```


Specifies whether to generate thumbnail from first page of the document or first image.

 **Remarks:** 

Default is  true , which means thumbnail will be generated from first page of the document. If value is  false  and there is no image in the document, thumbnail will be generated from first page of the document.

 **Examples:** 

Shows how to update a document's thumbnail.

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
boolean - The corresponding  boolean  value.
### getThumbnailSize() {#getThumbnailSize}
```
public Dimension getThumbnailSize()
```


Size of generated thumbnail in pixels. Default is 600x900.

 **Examples:** 

Shows how to update a document's thumbnail.

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
java.awt.Dimension - The corresponding java.awt.Dimension value.
### setGenerateFromFirstPage(boolean value) {#setGenerateFromFirstPage-boolean}
```
public void setGenerateFromFirstPage(boolean value)
```


Specifies whether to generate thumbnail from first page of the document or first image.

 **Remarks:** 

Default is  true , which means thumbnail will be generated from first page of the document. If value is  false  and there is no image in the document, thumbnail will be generated from first page of the document.

 **Examples:** 

Shows how to update a document's thumbnail.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setThumbnailSize(Dimension value) {#setThumbnailSize-java.awt.Dimension}
```
public void setThumbnailSize(Dimension value)
```


Size of generated thumbnail in pixels. Default is 600x900.

 **Examples:** 

Shows how to update a document's thumbnail.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Dimension | The corresponding java.awt.Dimension value. |

