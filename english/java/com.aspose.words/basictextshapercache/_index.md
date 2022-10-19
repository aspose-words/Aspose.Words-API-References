---
title: BasicTextShaperCache
second_title: Aspose.Words for Java API Reference
description: 
type: docs
weight: 28
url: /java/com.aspose.words/basictextshapercache/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.ITextShaperFactory](../../com.aspose.words/itextshaperfactory)
```
public class BasicTextShaperCache implements ITextShaperFactory
```
## Constructors

| Constructor | Description |
| --- | --- |
| [BasicTextShaperCache(ITextShaperFactory factory)](#BasicTextShaperCache-com.aspose.words.ITextShaperFactory-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getTextShaper(String fontPath, int faceIndex)](#getTextShaper-java.lang.String-int-) |  |
| [getTextShaper(String fontId, byte[] fontBlob, int faceIndex)](#getTextShaper-java.lang.String-byte---int-) |  |
| [dispose()](#dispose--) |  |
### BasicTextShaperCache(ITextShaperFactory factory) {#BasicTextShaperCache-com.aspose.words.ITextShaperFactory-}
```
public BasicTextShaperCache(ITextShaperFactory factory)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| factory | [ITextShaperFactory](../../com.aspose.words/itextshaperfactory) |  |

### getTextShaper(String fontPath, int faceIndex) {#getTextShaper-java.lang.String-int-}
```
public ITextShaper getTextShaper(String fontPath, int faceIndex)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontPath | java.lang.String |  |
| faceIndex | int |  |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper)
### getTextShaper(String fontId, byte[] fontBlob, int faceIndex) {#getTextShaper-java.lang.String-byte---int-}
```
public ITextShaper getTextShaper(String fontId, byte[] fontBlob, int faceIndex)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontId | java.lang.String |  |
| fontBlob | byte[] |  |
| faceIndex | int |  |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper)
### dispose() {#dispose--}
```
public void dispose()
```




