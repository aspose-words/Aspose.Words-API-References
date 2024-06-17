---
title: FontSourceType
linktitle: FontSourceType
second_title: Aspose.Words for Java
description: Specifies the type of a font source in Java.
type: docs
weight: 316
url: /java/com.aspose.words/fontsourcetype/
---

**Inheritance:**
java.lang.Object
```
public class FontSourceType
```

Specifies the type of a font source.

 **Examples:** 

Shows how to use a font file in the local file system as a font source.

```

 FileFontSource fileFontSource = new FileFontSource(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{fileFontSource});

 Assert.assertEquals(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.getFilePath());
 Assert.assertEquals(FontSourceType.FONT_FILE, fileFontSource.getType());
 Assert.assertEquals(0, fileFontSource.getPriority());
 
```
## Fields

| Field | Description |
| --- | --- |
| [FONTS_FOLDER](#FONTS-FOLDER) | A [FolderFontSource](../../com.aspose.words/folderfontsource/) object that represents folder with font files. |
| [FONT_FILE](#FONT-FILE) | A [FileFontSource](../../com.aspose.words/filefontsource/) object that represents single font file. |
| [FONT_STREAM](#FONT-STREAM) | A [StreamFontSource](../../com.aspose.words/streamfontsource/) object that represents a stream with font data. |
| [MEMORY_FONT](#MEMORY-FONT) | A [MemoryFontSource](../../com.aspose.words/memoryfontsource/) object that represents single font in memory. |
| [SYSTEM_FONTS](#SYSTEM-FONTS) | A [SystemFontSource](../../com.aspose.words/systemfontsource/) object that represents all fonts installed to the system. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String fontSourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int fontSourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontSourceType)](#toString-int) |  |
### FONTS_FOLDER {#FONTS-FOLDER}
```
public static int FONTS_FOLDER
```


A [FolderFontSource](../../com.aspose.words/folderfontsource/) object that represents folder with font files.

### FONT_FILE {#FONT-FILE}
```
public static int FONT_FILE
```


A [FileFontSource](../../com.aspose.words/filefontsource/) object that represents single font file.

### FONT_STREAM {#FONT-STREAM}
```
public static int FONT_STREAM
```


A [StreamFontSource](../../com.aspose.words/streamfontsource/) object that represents a stream with font data.

### MEMORY_FONT {#MEMORY-FONT}
```
public static int MEMORY_FONT
```


A [MemoryFontSource](../../com.aspose.words/memoryfontsource/) object that represents single font in memory.

### SYSTEM_FONTS {#SYSTEM-FONTS}
```
public static int SYSTEM_FONTS
```


A [SystemFontSource](../../com.aspose.words/systemfontsource/) object that represents all fonts installed to the system.

### length {#length}
```
public static int length
```


### fromName(String fontSourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String fontSourceTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontSourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int fontSourceType) {#getName-int}
```
public static String getName(int fontSourceType)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| fontSourceType | int |  |

**Returns:**
java.lang.String
