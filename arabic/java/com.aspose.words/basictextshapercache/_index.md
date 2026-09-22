---
title: "BasicTextShaperCache"
linktitle: "BasicTextShaperCache"
second_title: "Aspose.Words لـ Java"
description: "ينفذ ذاكرة تخزين مؤقت أساسية لكائنات ITextShaper في Java."
type: docs
weight: 37
url: /ar/java/com.aspose.words/basictextshapercache/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.ITextShaperFactory](../../com.aspose.words/itextshaperfactory/)
```
public class BasicTextShaperCache implements ITextShaperFactory
```

ينفذ ذاكرة تخزين مؤقت أساسية لكائنات [ITextShaper](../../com.aspose.words/itextshaper/) . هذه الفئة آمنة للخيوط.
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [BasicTextShaperCache(ITextShaperFactory factory)](#BasicTextShaperCache-com.aspose.words.ITextShaperFactory) | يغلف المصنع ويخزن نتائج [ITextShaperFactory.getTextShaper(java.lang.String, int)](../../com.aspose.words/itextshaperfactory/\#getTextShaper-java.lang.String--int) في الذاكرة المؤقتة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [dispose()](#dispose) | يحرر كائنات [ITextShaper](../../com.aspose.words/itextshaper/) المخزنة مؤقتًا. |
| [getTextShaper(String fontId, byte[] fontBlob, int faceIndex)](#getTextShaper-java.lang.String-byte---int) |  |
| [getTextShaper(String fontPath, int faceIndex)](#getTextShaper-java.lang.String-int) |  |
### BasicTextShaperCache(ITextShaperFactory factory) {#BasicTextShaperCache-com.aspose.words.ITextShaperFactory}
```
public BasicTextShaperCache(ITextShaperFactory factory)
```


يغلف المصنع ويخزن نتائج [ITextShaperFactory.getTextShaper(java.lang.String, int)](../../com.aspose.words/itextshaperfactory/\#getTextShaper-java.lang.String--int) في الذاكرة المؤقتة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| factory | [ITextShaperFactory](../../com.aspose.words/itextshaperfactory/) |  |

### dispose() {#dispose}
```
public void dispose()
```


يحرر كائنات [ITextShaper](../../com.aspose.words/itextshaper/) المخزنة مؤقتًا.

### getTextShaper(String fontId, byte[] fontBlob, int faceIndex) {#getTextShaper-java.lang.String-byte---int}
```
public ITextShaper getTextShaper(String fontId, byte[] fontBlob, int faceIndex)
```


يعيد نسخة جديدة من مُشكِّل النص للخط الممثَّل بـ  fontBlob  و  faceIndex .

**Parameters:**
| معامل | نوع | الوصف |
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


يعيد نسخة جديدة من مُشكِّل النص للخط المحدد بـ  fontPath  و  faceIndex .

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fontPath | java.lang.String |  |
| faceIndex | int |  |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
