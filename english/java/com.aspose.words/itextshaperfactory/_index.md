---
title: ITextShaperFactory
linktitle: ITextShaperFactory
second_title: Aspose.Words for Java
description: An interface of a factory for constructing ITextShaper implementations in Java.
type: docs
weight: 784
url: /java/com.aspose.words/itextshaperfactory/
---
```
public interface ITextShaperFactory
```

An interface of a factory for constructing [ITextShaper](../../com.aspose.words/itextshaper/) implementations.
## Methods

| Method | Description |
| --- | --- |
| [getTextShaper(String fontId, byte[] fontBlob, int faceIndex)](#getTextShaper-java.lang.String-byte---int) | Returns new instance of a text shaper for the font represented by  fontBlob  and  faceIndex . |
| [getTextShaper(String fontPath, int faceIndex)](#getTextShaper-java.lang.String-int) | Returns new instance of a text shaper for the font specified by  fontPath  and  faceIndex . |
### getTextShaper(String fontId, byte[] fontBlob, int faceIndex) {#getTextShaper-java.lang.String-byte---int}
```
public abstract ITextShaper getTextShaper(String fontId, byte[] fontBlob, int faceIndex)
```


Returns new instance of a text shaper for the font represented by  fontBlob  and  faceIndex .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontId | java.lang.String | A unique identifier that can be uniquely associated with the provided font  fontBlob . |
| fontBlob | byte[] | Byte array with the font data. |
| faceIndex | int | An index of the font face in the TrueType font collection, or 0 if  fontBlob  is not TrueType font collection. |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
### getTextShaper(String fontPath, int faceIndex) {#getTextShaper-java.lang.String-int}
```
public abstract ITextShaper getTextShaper(String fontPath, int faceIndex)
```


Returns new instance of a text shaper for the font specified by  fontPath  and  faceIndex .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontPath | java.lang.String | An absolute path to the font file. |
| faceIndex | int | An index of the font face in the TrueType font collection, or 0 if specified font file is not TrueType font collection. |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
