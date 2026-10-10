---
title: "FontSourceType"
linktitle: "FontSourceType"
second_title: "Aspose.Words per Java"
description: "Specifica il tipo di origine font in Java."
type: docs
weight: 334
url: /it/java/com.aspose.words/fontsourcetype/
---

**Inheritance:**
java.lang.Object
```
public class FontSourceType
```

Specifica il tipo di origine del font.

 **Examples:** 

Mostra come utilizzare un file di carattere nel file system locale come sorgente di caratteri.

```

 FileFontSource fileFontSource = new FileFontSource(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{fileFontSource});

 Assert.assertEquals(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.getFilePath());
 Assert.assertEquals(FontSourceType.FONT_FILE, fileFontSource.getType());
 Assert.assertEquals(0, fileFontSource.getPriority());
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [FONTS_FOLDER](#FONTS-FOLDER) | Un oggetto [FolderFontSource](../../com.aspose.words/folderfontsource/) che rappresenta una cartella con file di font. |
| [FONT_FILE](#FONT-FILE) | Un oggetto [FileFontSource](../../com.aspose.words/filefontsource/) che rappresenta un singolo file di font. |
| [FONT_STREAM](#FONT-STREAM) | Un oggetto [StreamFontSource](../../com.aspose.words/streamfontsource/) che rappresenta un flusso con dati di font. |
| [MEMORY_FONT](#MEMORY-FONT) | Un oggetto [MemoryFontSource](../../com.aspose.words/memoryfontsource/) che rappresenta un singolo font in memoria. |
| [SYSTEM_FONTS](#SYSTEM-FONTS) | Un oggetto [SystemFontSource](../../com.aspose.words/systemfontsource/) che rappresenta tutti i font installati nel sistema. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String fontSourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int fontSourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontSourceType)](#toString-int) |  |
### FONTS_FOLDER {#FONTS-FOLDER}
```
public static int FONTS_FOLDER
```


Un oggetto [FolderFontSource](../../com.aspose.words/folderfontsource/) che rappresenta una cartella con file di font.

### FONT_FILE {#FONT-FILE}
```
public static int FONT_FILE
```


Un oggetto [FileFontSource](../../com.aspose.words/filefontsource/) che rappresenta un singolo file di font.

### FONT_STREAM {#FONT-STREAM}
```
public static int FONT_STREAM
```


Un oggetto [StreamFontSource](../../com.aspose.words/streamfontsource/) che rappresenta un flusso con dati di font.

### MEMORY_FONT {#MEMORY-FONT}
```
public static int MEMORY_FONT
```


Un oggetto [MemoryFontSource](../../com.aspose.words/memoryfontsource/) che rappresenta un singolo font in memoria.

### SYSTEM_FONTS {#SYSTEM-FONTS}
```
public static int SYSTEM_FONTS
```


Un oggetto [SystemFontSource](../../com.aspose.words/systemfontsource/) che rappresenta tutti i font installati nel sistema.

### length {#length}
```
public static int length
```


### fromName(String fontSourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String fontSourceTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontSourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int fontSourceType) {#getName-int}
```
public static String getName(int fontSourceType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontSourceType | int |  |

**Returns:**
java.lang.String
