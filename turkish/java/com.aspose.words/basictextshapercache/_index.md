---
title: "BasicTextShaperCache"
linktitle: "BasicTextShaperCache"
second_title: "Aspose.Words Java için"
description: "Java'da ITextShaper örnekleri için temel önbelleği uygular."
type: docs
weight: 37
url: /tr/java/com.aspose.words/basictextshapercache/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.ITextShaperFactory](../../com.aspose.words/itextshaperfactory/)
```
public class BasicTextShaperCache implements ITextShaperFactory
```

İlgili [ITextShaper](../../com.aspose.words/itextshaper/) örnekleri için temel önbelleği uygular. Bu sınıf çok iş parçacıklı güvenlidir.
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [BasicTextShaperCache(ITextShaperFactory factory)](#BasicTextShaperCache-com.aspose.words.ITextShaperFactory) | Fabrika'yı sarar ve [ITextShaperFactory.getTextShaper(java.lang.String, int)](../../com.aspose.words/itextshaperfactory/\\#getTextShaper-java.lang.String--int) sonuçlarını önbelleğe alır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [dispose()](#dispose) | Önbelleğe alınmış [ITextShaper](../../com.aspose.words/itextshaper/) örneklerini serbest bırakır. |
| [getTextShaper(String fontId, byte[] fontBlob, int faceIndex)](#getTextShaper-java.lang.String-byte---int) |  |
| [getTextShaper(String fontPath, int faceIndex)](#getTextShaper-java.lang.String-int) |  |
### BasicTextShaperCache(ITextShaperFactory factory) {#BasicTextShaperCache-com.aspose.words.ITextShaperFactory}
```
public BasicTextShaperCache(ITextShaperFactory factory)
```


Fabrika'yı sarar ve [ITextShaperFactory.getTextShaper(java.lang.String, int)](../../com.aspose.words/itextshaperfactory/\\#getTextShaper-java.lang.String--int) sonuçlarını önbelleğe alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| factory | [ITextShaperFactory](../../com.aspose.words/itextshaperfactory/) |  |

### dispose() {#dispose}
```
public void dispose()
```


Önbelleğe alınmış [ITextShaper](../../com.aspose.words/itextshaper/) örneklerini serbest bırakır.

### getTextShaper(String fontId, byte[] fontBlob, int faceIndex) {#getTextShaper-java.lang.String-byte---int}
```
public ITextShaper getTextShaper(String fontId, byte[] fontBlob, int faceIndex)
```


  fontBlob  ve  faceIndex  tarafından temsil edilen yazı tipi için yeni bir metin şekillendirici örneği döndürür.

**Parameters:**
| Parametre | Tür | Açıklama |
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


  fontPath  ve  faceIndex  tarafından belirtilen yazı tipi için yeni bir metin şekillendirici örneği döndürür.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontPath | java.lang.String |  |
| faceIndex | int |  |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
