---
title: ITextShaperFactory
second_title: Aspose.Words for Java API Reference
description: 
type: docs
weight: 660
url: /zh/java/com.aspose.words/itextshaperfactory/
---
```
public interface ITextShaperFactory
```
## 方法

| 方法 | 描述 |
| --- | --- |
| [getTextShaper(String fontId, byte[] fontBlob, int faceIndex)](#getTextShaper-java.lang.String-byte---int-) |  |
| [getTextShaper(String fontPath, int faceIndex)](#getTextShaper-java.lang.String-int-) |  |
### getTextShaper(String fontId, byte[] fontBlob, int faceIndex) {#getTextShaper-java.lang.String-byte---int-}
```
public abstract ITextShaper getTextShaper(String fontId, byte[] fontBlob, int faceIndex)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontId | java.lang.String |  |
| fontBlob | byte[] |  |
| faceIndex | int |  |

**退货:**
[ITextShaper](../../com.aspose.words/itextshaper)
### getTextShaper(String fontPath, int faceIndex) {#getTextShaper-java.lang.String-int-}
```
public abstract ITextShaper getTextShaper(String fontPath, int faceIndex)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontPath | java.lang.String |  |
| faceIndex | int |  |

**退货:**
[ITextShaper](../../com.aspose.words/itextshaper)