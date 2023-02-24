---
title: ThumbnailGeneratingOptions
linktitle: ThumbnailGeneratingOptions
second_title: Aspose.Words for Java API Reference
description: Can be used to specify additional options when generating thumbnail for a document in Java.
type: docs
weight: 584
url: /java/com.aspose.words/thumbnailgeneratingoptions/
---

**Inheritance:**
java.lang.Object
```
public class ThumbnailGeneratingOptions
```

Can be used to specify additional options when generating thumbnail for a document. User can call method [Document.updateThumbnail(com.aspose.words.ThumbnailGeneratingOptions)](../../com.aspose.words/document/\#updateThumbnail-com.aspose.words.ThumbnailGeneratingOptions) to generate [BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties/\#getThumbnail) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties/\#setThumbnail-byte) for a document.
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getGenerateFromFirstPage()](#getGenerateFromFirstPage) | Specifies whether to generate thumbnail from first page of the document or first image. |
| [getThumbnailSize()](#getThumbnailSize) | Size of generated thumbnail in pixels. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setGenerateFromFirstPage(boolean value)](#setGenerateFromFirstPage-boolean) | Specifies whether to generate thumbnail from first page of the document or first image. |
| [setThumbnailSize(Dimension value)](#setThumbnailSize-java.awt.Dimension) | Size of generated thumbnail in pixels. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getGenerateFromFirstPage() {#getGenerateFromFirstPage}
```
public boolean getGenerateFromFirstPage()
```


Specifies whether to generate thumbnail from first page of the document or first image. Default is  true , which means thumbnail will be generated from first page of the document. If value is  false  and there is no image in the document, thumbnail will be generated from first page of the document.

**Returns:**
boolean - The corresponding  boolean  value.
### getThumbnailSize() {#getThumbnailSize}
```
public Dimension getThumbnailSize()
```


Size of generated thumbnail in pixels. Default is 600x900.

**Returns:**
java.awt.Dimension - The corresponding java.awt.Dimension value.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### setGenerateFromFirstPage(boolean value) {#setGenerateFromFirstPage-boolean}
```
public void setGenerateFromFirstPage(boolean value)
```


Specifies whether to generate thumbnail from first page of the document or first image. Default is  true , which means thumbnail will be generated from first page of the document. If value is  false  and there is no image in the document, thumbnail will be generated from first page of the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setThumbnailSize(Dimension value) {#setThumbnailSize-java.awt.Dimension}
```
public void setThumbnailSize(Dimension value)
```


Size of generated thumbnail in pixels. Default is 600x900.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Dimension | The corresponding java.awt.Dimension value. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

