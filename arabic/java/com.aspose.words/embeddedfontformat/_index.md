---
title: "EmbeddedFontFormat"
linktitle: "EmbeddedFontFormat"
second_title: "Aspose.Words لـ Java"
description: "يحدد تنسيق خط مضمّن معين داخل كائن FontInfo في جافا."
type: docs
weight: 184
url: /ar/java/com.aspose.words/embeddedfontformat/
---

**Inheritance:**
java.lang.Object
```
public class EmbeddedFontFormat
```

يحدد تنسيق خط مضمّن معين داخل كائن [FontInfo](../../com.aspose.words/fontinfo/) .

عند حفظ مستند إلى ملف، يتم كتابة الخطوط المضمّنة ذات التنسيق المقابل فقط.

 **Examples:** 

يوضح كيفية استخراج خط مضمّن من مستند وحفظه في نظام الملفات المحلي.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfo embeddedFont = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift");
 byte[] embeddedFontBytes = embeddedFont.getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR);
 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.ttf"), embeddedFontBytes);

 // Embedded font formats may be different in other formats such as .doc.
 // We need to know the correct format before we can extract the font.
 doc = new Document(getMyDir() + "Embedded font.doc");

 Assert.assertNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR));
 Assert.assertNotNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.EMBEDDED_OPEN_TYPE, EmbeddedFontStyle.REGULAR));

 // Also, we can convert embedded OpenType format, which comes from .doc documents, to OpenType.
 embeddedFontBytes = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFontAsOpenType(EmbeddedFontStyle.REGULAR);

 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.otf"), embeddedFontBytes);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [EMBEDDED_OPEN_TYPE](#EMBEDDED-OPEN-TYPE) | يحدد تنسيق ملف Embedded OpenType (EOT). |
| [OPEN_TYPE](#OPEN-TYPE) | يحدد الخط المضمّن كنسخة عادية من ملف خط OpenType (TrueType). |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String embeddedFontFormatName)](#fromName-java.lang.String) |  |
| [getName(int embeddedFontFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int embeddedFontFormat)](#toString-int) |  |
### EMBEDDED_OPEN_TYPE {#EMBEDDED-OPEN-TYPE}
```
public static int EMBEDDED_OPEN_TYPE
```


يحدد تنسيق ملف Embedded OpenType (EOT).

يُستخدم هذا التنسيق للخطوط المضمّنة في ملفات DOC.

 **Remarks:** 

انظر http://www.w3.org/Submission/EOT للحصول على وصف التنسيق.

### OPEN_TYPE {#OPEN-TYPE}
```
public static int OPEN_TYPE
```


يحدد الخط المضمّن كنسخة عادية من ملف خط OpenType (TrueType).

هذا التنسيق للخطوط المدمجة يُستخدم في تنسيق Open Office XML، بما في ذلك ملفات DOCX.

### length {#length}
```
public static int length
```


### fromName(String embeddedFontFormatName) {#fromName-java.lang.String}
```
public static int fromName(String embeddedFontFormatName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| embeddedFontFormatName | java.lang.String |  |

**Returns:**
int
### getName(int embeddedFontFormat) {#getName-int}
```
public static String getName(int embeddedFontFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| embeddedFontFormat | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int embeddedFontFormat) {#toString-int}
```
public static String toString(int embeddedFontFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| embeddedFontFormat | int |  |

**Returns:**
java.lang.String
