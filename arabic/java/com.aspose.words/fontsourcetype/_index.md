---
title: "FontSourceType"
linktitle: "FontSourceType"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع مصدر الخط في Java."
type: docs
weight: 334
url: /ar/java/com.aspose.words/fontsourcetype/
---

**Inheritance:**
java.lang.Object
```
public class FontSourceType
```

يحدد نوع مصدر الخط.

 **Examples:** 

يوضح كيفية استخدام ملف خط في نظام الملفات المحلي كمصدر للخط.

```

 FileFontSource fileFontSource = new FileFontSource(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{fileFontSource});

 Assert.assertEquals(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.getFilePath());
 Assert.assertEquals(FontSourceType.FONT_FILE, fileFontSource.getType());
 Assert.assertEquals(0, fileFontSource.getPriority());
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [FONTS_FOLDER](#FONTS-FOLDER) | كائن [FolderFontSource](../../com.aspose.words/folderfontsource/) يمثل مجلدًا يحتوي على ملفات الخطوط. |
| [FONT_FILE](#FONT-FILE) | كائن [FileFontSource](../../com.aspose.words/filefontsource/) يمثل ملف خط واحد. |
| [FONT_STREAM](#FONT-STREAM) | كائن [StreamFontSource](../../com.aspose.words/streamfontsource/) يمثل تدفقًا يحتوي على بيانات الخط. |
| [MEMORY_FONT](#MEMORY-FONT) | كائن [MemoryFontSource](../../com.aspose.words/memoryfontsource/) يمثل خطًا واحدًا في الذاكرة. |
| [SYSTEM_FONTS](#SYSTEM-FONTS) | كائن [SystemFontSource](../../com.aspose.words/systemfontsource/) يمثل جميع الخطوط المثبتة على النظام. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String fontSourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int fontSourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontSourceType)](#toString-int) |  |
### FONTS_FOLDER {#FONTS-FOLDER}
```
public static int FONTS_FOLDER
```


كائن [FolderFontSource](../../com.aspose.words/folderfontsource/) يمثل مجلدًا يحتوي على ملفات الخطوط.

### FONT_FILE {#FONT-FILE}
```
public static int FONT_FILE
```


كائن [FileFontSource](../../com.aspose.words/filefontsource/) يمثل ملف خط واحد.

### FONT_STREAM {#FONT-STREAM}
```
public static int FONT_STREAM
```


كائن [StreamFontSource](../../com.aspose.words/streamfontsource/) يمثل تدفقًا يحتوي على بيانات الخط.

### MEMORY_FONT {#MEMORY-FONT}
```
public static int MEMORY_FONT
```


كائن [MemoryFontSource](../../com.aspose.words/memoryfontsource/) يمثل خطًا واحدًا في الذاكرة.

### SYSTEM_FONTS {#SYSTEM-FONTS}
```
public static int SYSTEM_FONTS
```


كائن [SystemFontSource](../../com.aspose.words/systemfontsource/) يمثل جميع الخطوط المثبتة على النظام.

### length {#length}
```
public static int length
```


### fromName(String fontSourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String fontSourceTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fontSourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int fontSourceType) {#getName-int}
```
public static String getName(int fontSourceType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fontSourceType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int fontSourceType) {#toString-int}
```
public static String toString(int fontSourceType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fontSourceType | int |  |

**Returns:**
java.lang.String
