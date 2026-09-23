---
title: "FontSourceType"
linktitle: "FontSourceType"
second_title: "Aspose.Words für Java"
description: "Gibt den Typ der Schriftquellen in Java an."
type: docs
weight: 334
url: /de/java/com.aspose.words/fontsourcetype/
---

**Inheritance:**
java.lang.Object
```
public class FontSourceType
```

Gibt den Typ der Schriftquelle an.

 **Examples:** 

Zeigt, wie eine Schriftdatei im lokalen Dateisystem als Schriftquelle verwendet wird.

```

 FileFontSource fileFontSource = new FileFontSource(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{fileFontSource});

 Assert.assertEquals(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.getFilePath());
 Assert.assertEquals(FontSourceType.FONT_FILE, fileFontSource.getType());
 Assert.assertEquals(0, fileFontSource.getPriority());
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [FONTS_FOLDER](#FONTS-FOLDER) | Ein [FolderFontSource](../../com.aspose.words/folderfontsource/) Objekt, das einen Ordner mit Schriftdateien darstellt. |
| [FONT_FILE](#FONT-FILE) | Ein [FileFontSource](../../com.aspose.words/filefontsource/) Objekt, das eine einzelne Schriftdatei darstellt. |
| [FONT_STREAM](#FONT-STREAM) | Ein [StreamFontSource](../../com.aspose.words/streamfontsource/) Objekt, das einen Stream mit Schriftartdaten darstellt. |
| [MEMORY_FONT](#MEMORY-FONT) | Ein [MemoryFontSource](../../com.aspose.words/memoryfontsource/) Objekt, das eine einzelne Schriftart im Speicher darstellt. |
| [SYSTEM_FONTS](#SYSTEM-FONTS) | Ein [SystemFontSource](../../com.aspose.words/systemfontsource/) Objekt, das alle im System installierten Schriften darstellt. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String fontSourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int fontSourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontSourceType)](#toString-int) |  |
### FONTS_FOLDER {#FONTS-FOLDER}
```
public static int FONTS_FOLDER
```


Ein [FolderFontSource](../../com.aspose.words/folderfontsource/) Objekt, das einen Ordner mit Schriftdateien darstellt.

### FONT_FILE {#FONT-FILE}
```
public static int FONT_FILE
```


Ein [FileFontSource](../../com.aspose.words/filefontsource/) Objekt, das eine einzelne Schriftdatei darstellt.

### FONT_STREAM {#FONT-STREAM}
```
public static int FONT_STREAM
```


Ein [StreamFontSource](../../com.aspose.words/streamfontsource/) Objekt, das einen Stream mit Schriftartdaten darstellt.

### MEMORY_FONT {#MEMORY-FONT}
```
public static int MEMORY_FONT
```


Ein [MemoryFontSource](../../com.aspose.words/memoryfontsource/) Objekt, das eine einzelne Schriftart im Speicher darstellt.

### SYSTEM_FONTS {#SYSTEM-FONTS}
```
public static int SYSTEM_FONTS
```


Ein [SystemFontSource](../../com.aspose.words/systemfontsource/) Objekt, das alle im System installierten Schriften darstellt.

### length {#length}
```
public static int length
```


### fromName(String fontSourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String fontSourceTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontSourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int fontSourceType) {#getName-int}
```
public static String getName(int fontSourceType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontSourceType | int |  |

**Returns:**
java.lang.String
