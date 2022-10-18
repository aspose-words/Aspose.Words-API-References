---
title: ThumbnailGeneratingOptions
second_title: Aspose.Words for Java API Reference
description: Can be used to specify additional options when generating thumbnail for a document.
type: docs
weight: 578
url: /java/com.aspose.words/thumbnailgeneratingoptions/
---

**Inheritance:**
java.lang.Object
```
public class ThumbnailGeneratingOptions
```

Can be used to specify additional options when generating thumbnail for a document. User can call method [Document.updateThumbnail(com.aspose.words.ThumbnailGeneratingOptions)](../../com.aspose.words/document\#updateThumbnail-com.aspose.words.ThumbnailGeneratingOptions-) to generate [BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties\#getThumbnail--) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties\#setThumbnail-byte---) for a document.
## Methods

| Method | Description |
| --- | --- |
| [getGenerateFromFirstPage()](#getGenerateFromFirstPage--) | Specifies whether to generate thumbnail from first page of the document or first image. |
| [setGenerateFromFirstPage(boolean value)](#setGenerateFromFirstPage-boolean-) | Specifies whether to generate thumbnail from first page of the document or first image. |
| [getThumbnailSize()](#getThumbnailSize--) | Size of generated thumbnail in pixels. |
| [setThumbnailSize(Dimension value)](#setThumbnailSize-java.awt.Dimension-) | Size of generated thumbnail in pixels. |
### getGenerateFromFirstPage() {#getGenerateFromFirstPage--}
```
public boolean getGenerateFromFirstPage()
```


Specifies whether to generate thumbnail from first page of the document or first image. Default is  true , which means thumbnail will be generated from first page of the document. If value is  false  and there is no image in the document, thumbnail will be generated from first page of the document.

**Returns:**
boolean - The corresponding  boolean  value.
### setGenerateFromFirstPage(boolean value) {#setGenerateFromFirstPage-boolean-}
```
public void setGenerateFromFirstPage(boolean value)
```


Specifies whether to generate thumbnail from first page of the document or first image. Default is  true , which means thumbnail will be generated from first page of the document. If value is  false  and there is no image in the document, thumbnail will be generated from first page of the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getThumbnailSize() {#getThumbnailSize--}
```
public Dimension getThumbnailSize()
```


Size of generated thumbnail in pixels. Default is 600x900.

**Returns:**
java.awt.Dimension - The corresponding java.awt.Dimension value.
### setThumbnailSize(Dimension value) {#setThumbnailSize-java.awt.Dimension-}
```
public void setThumbnailSize(Dimension value)
```


Size of generated thumbnail in pixels. Default is 600x900.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Dimension | The corresponding java.awt.Dimension value. |

