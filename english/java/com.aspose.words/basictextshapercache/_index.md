---
title: BasicTextShaperCache
linktitle: BasicTextShaperCache
second_title: Aspose.Words for Java
description: Implements basic cache for ITextShaper instances in Java.
type: docs
weight: 36
url: /java/com.aspose.words/basictextshapercache/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.ITextShaperFactory](../../com.aspose.words/itextshaperfactory/)
```
public class BasicTextShaperCache implements ITextShaperFactory
```

Implements basic cache for [ITextShaper](../../com.aspose.words/itextshaper/) instances. This class is thread-safe.
## Constructors

| Constructor | Description |
| --- | --- |
| [BasicTextShaperCache(ITextShaperFactory factory)](#BasicTextShaperCache-com.aspose.words.ITextShaperFactory) | Wraps  factory  and caches [ITextShaperFactory.getTextShaper(java.lang.String, int)](../../com.aspose.words/itextshaperfactory/\#getTextShaper-java.lang.String--int) results. |
## Methods

| Method | Description |
| --- | --- |
| [dispose()](#dispose) |  |
| [getTextShaper(String fontId, byte[] fontBlob, int faceIndex)](#getTextShaper-java.lang.String-byte---int) |  |
| [getTextShaper(String fontPath, int faceIndex)](#getTextShaper-java.lang.String-int) |  |
### BasicTextShaperCache(ITextShaperFactory factory) {#BasicTextShaperCache-com.aspose.words.ITextShaperFactory}
```
public BasicTextShaperCache(ITextShaperFactory factory)
```


Wraps  factory  and caches [ITextShaperFactory.getTextShaper(java.lang.String, int)](../../com.aspose.words/itextshaperfactory/\#getTextShaper-java.lang.String--int) results.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| factory | [ITextShaperFactory](../../com.aspose.words/itextshaperfactory/) |  |

### dispose() {#dispose}
```
public void dispose()
```




### getTextShaper(String fontId, byte[] fontBlob, int faceIndex) {#getTextShaper-java.lang.String-byte---int}
```
public ITextShaper getTextShaper(String fontId, byte[] fontBlob, int faceIndex)
```


Returns new instance of a text shaper for the font represented by  fontBlob  and  faceIndex .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontId | java.lang.String |  |
| fontBlob | byte[] |  |
| faceIndex | int |  |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
### getTextShaper(String fontPath, int faceIndex) {#getTextShaper-java.lang.String-int}
```
public ITextShaper getTextShaper(String fontPath, int faceIndex)
```


Returns new instance of a text shaper for the font specified by  fontPath  and  faceIndex .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontPath | java.lang.String |  |
| faceIndex | int |  |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
