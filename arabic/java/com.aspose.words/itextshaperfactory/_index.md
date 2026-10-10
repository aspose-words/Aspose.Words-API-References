---
title: "ITextShaperFactory"
linktitle: "ITextShaperFactory"
second_title: "Aspose.Words لـ Java"
description: "واجهة مصنع لإنشاء تطبيقات ITextShaper في Java."
type: docs
weight: 787
url: /ar/java/com.aspose.words/itextshaperfactory/
---
```
public interface ITextShaperFactory
```

واجهة مصنع لإنشاء تطبيقات [ITextShaper](../../com.aspose.words/itextshaper/).
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getTextShaper(String fontId, byte[] fontBlob, int faceIndex)](#getTextShaper-java.lang.String-byte---int) | يعيد نسخة جديدة من مُشكِّل النص للخط الممثَّل بـ  fontBlob  و  faceIndex . |
| [getTextShaper(String fontPath, int faceIndex)](#getTextShaper-java.lang.String-int) | يعيد نسخة جديدة من مُشكِّل النص للخط المحدد بـ  fontPath  و  faceIndex . |
### getTextShaper(String fontId, byte[] fontBlob, int faceIndex) {#getTextShaper-java.lang.String-byte---int}
```
public abstract ITextShaper getTextShaper(String fontId, byte[] fontBlob, int faceIndex)
```


يعيد نسخة جديدة من مُشكِّل النص للخط الممثَّل بـ  fontBlob  و  faceIndex .

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fontId | java.lang.String | معرف فريد يمكن ربطه بشكل فريد مع الخط المقدم fontBlob. |
| fontBlob | byte[] | مصفوفة بايت تحتوي على بيانات الخط. |
| faceIndex | int | فهرس لوجه الخط في مجموعة خطوط TrueType، أو 0 إذا كان  fontBlob  ليس مجموعة خطوط TrueType. |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
### getTextShaper(String fontPath, int faceIndex) {#getTextShaper-java.lang.String-int}
```
public abstract ITextShaper getTextShaper(String fontPath, int faceIndex)
```


يعيد نسخة جديدة من مُشكِّل النص للخط المحدد بـ  fontPath  و  faceIndex .

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fontPath | java.lang.String | مسار مطلق لملف الخط. |
| faceIndex | int | فهرس لوجه الخط في مجموعة خطوط TrueType، أو 0 إذا كان ملف الخط المحدد ليس مجموعة خطوط TrueType. |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
