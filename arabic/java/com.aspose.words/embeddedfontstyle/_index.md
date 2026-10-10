---
title: "EmbeddedFontStyle"
linktitle: "EmbeddedFontStyle"
second_title: "Aspose.Words لـ Java"
description: "يحدد نمط الخط المضمن داخل كائن FontInfo في جافا."
type: docs
weight: 185
url: /ar/java/com.aspose.words/embeddedfontstyle/
---

**Inheritance:**
java.lang.Object
```
public class EmbeddedFontStyle
```

يحدد نمط الخط المضمن داخل كائن [FontInfo](../../com.aspose.words/fontinfo/).

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
| [BOLD](#BOLD) | يحدد الخط المضمن الغامق. |
| [BOLD_ITALIC](#BOLD-ITALIC) | يحدد الخط المضمن الغامق المائل. |
| [ITALIC](#ITALIC) | يحدد الخط المضمن المائل. |
| [REGULAR](#REGULAR) | يحدد الخط المضمن العادي. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String embeddedFontStyleName)](#fromName-java.lang.String) |  |
| [fromNames(Set embeddedFontStyleNames)](#fromNames-java.util.Set) |  |
| [getName(int embeddedFontStyle)](#getName-int) |  |
| [getNames(int embeddedFontStyle)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int embeddedFontStyle)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### BOLD {#BOLD}
```
public static int BOLD
```


يحدد الخط المضمن الغامق.

### BOLD_ITALIC {#BOLD-ITALIC}
```
public static int BOLD_ITALIC
```


يحدد الخط المضمن الغامق المائل.

### ITALIC {#ITALIC}
```
public static int ITALIC
```


يحدد الخط المضمن المائل.

### REGULAR {#REGULAR}
```
public static int REGULAR
```


يحدد الخط المضمن العادي.

### length {#length}
```
public static int length
```


### fromName(String embeddedFontStyleName) {#fromName-java.lang.String}
```
public static int fromName(String embeddedFontStyleName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| embeddedFontStyleName | java.lang.String |  |

**Returns:**
int
### fromNames(Set embeddedFontStyleNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set embeddedFontStyleNames)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| embeddedFontStyleNames | java.util.Set |  |

**Returns:**
int
### getName(int embeddedFontStyle) {#getName-int}
```
public static String getName(int embeddedFontStyle)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| embeddedFontStyle | int |  |

**Returns:**
java.lang.String
### getNames(int embeddedFontStyle) {#getNames-int}
```
public static Set getNames(int embeddedFontStyle)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| embeddedFontStyle | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int embeddedFontStyle) {#toString-int}
```
public static String toString(int embeddedFontStyle)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| embeddedFontStyle | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
