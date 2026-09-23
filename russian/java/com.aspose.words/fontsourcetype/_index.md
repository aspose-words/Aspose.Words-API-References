---
title: "FontSourceType"
linktitle: "FontSourceType"
second_title: "Aspose.Words для Java"
description: "Указывает тип источника шрифтов в Java."
type: docs
weight: 334
url: /ru/java/com.aspose.words/fontsourcetype/
---

**Inheritance:**
java.lang.Object
```
public class FontSourceType
```

Указывает тип источника шрифта.

 **Examples:** 

Показывает, как использовать файл шрифта в локальной файловой системе в качестве источника шрифтов.

```

 FileFontSource fileFontSource = new FileFontSource(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{fileFontSource});

 Assert.assertEquals(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.getFilePath());
 Assert.assertEquals(FontSourceType.FONT_FILE, fileFontSource.getType());
 Assert.assertEquals(0, fileFontSource.getPriority());
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [FONTS_FOLDER](#FONTS-FOLDER) | Объект [FolderFontSource](../../com.aspose.words/folderfontsource/) , представляющий папку с файлами шрифтов. |
| [FONT_FILE](#FONT-FILE) | Объект [FileFontSource](../../com.aspose.words/filefontsource/) , представляющий отдельный файл шрифта. |
| [FONT_STREAM](#FONT-STREAM) | Объект [StreamFontSource](../../com.aspose.words/streamfontsource/) , представляющий поток с данными шрифта. |
| [MEMORY_FONT](#MEMORY-FONT) | Объект [MemoryFontSource](../../com.aspose.words/memoryfontsource/) , представляющий отдельный шрифт в памяти. |
| [SYSTEM_FONTS](#SYSTEM-FONTS) | Объект [SystemFontSource](../../com.aspose.words/systemfontsource/) , представляющий все шрифты, установленные в системе. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String fontSourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int fontSourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontSourceType)](#toString-int) |  |
### FONTS_FOLDER {#FONTS-FOLDER}
```
public static int FONTS_FOLDER
```


Объект [FolderFontSource](../../com.aspose.words/folderfontsource/) , представляющий папку с файлами шрифтов.

### FONT_FILE {#FONT-FILE}
```
public static int FONT_FILE
```


Объект [FileFontSource](../../com.aspose.words/filefontsource/) , представляющий отдельный файл шрифта.

### FONT_STREAM {#FONT-STREAM}
```
public static int FONT_STREAM
```


Объект [StreamFontSource](../../com.aspose.words/streamfontsource/) , представляющий поток с данными шрифта.

### MEMORY_FONT {#MEMORY-FONT}
```
public static int MEMORY_FONT
```


Объект [MemoryFontSource](../../com.aspose.words/memoryfontsource/) , представляющий отдельный шрифт в памяти.

### SYSTEM_FONTS {#SYSTEM-FONTS}
```
public static int SYSTEM_FONTS
```


Объект [SystemFontSource](../../com.aspose.words/systemfontsource/) , представляющий все шрифты, установленные в системе.

### length {#length}
```
public static int length
```


### fromName(String fontSourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String fontSourceTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fontSourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int fontSourceType) {#getName-int}
```
public static String getName(int fontSourceType)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| fontSourceType | int |  |

**Returns:**
java.lang.String
