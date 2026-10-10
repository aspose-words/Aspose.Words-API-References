---
title: "FontSourceType"
linktitle: "FontSourceType"
second_title: "Aspose.Words para Java"
description: "Especifica el tipo de origen de fuente en Java."
type: docs
weight: 334
url: /es/java/com.aspose.words/fontsourcetype/
---

**Inheritance:**
java.lang.Object
```
public class FontSourceType
```

Especifica el tipo de origen de fuente.

 **Examples:** 

Muestra cómo usar un archivo de fuente en el sistema de archivos local como una fuente de fuentes.

```

 FileFontSource fileFontSource = new FileFontSource(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{fileFontSource});

 Assert.assertEquals(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.getFilePath());
 Assert.assertEquals(FontSourceType.FONT_FILE, fileFontSource.getType());
 Assert.assertEquals(0, fileFontSource.getPriority());
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [FONTS_FOLDER](#FONTS-FOLDER) | Un objeto [FolderFontSource](../../com.aspose.words/folderfontsource/) que representa una carpeta con archivos de fuentes. |
| [FONT_FILE](#FONT-FILE) | Un objeto [FileFontSource](../../com.aspose.words/filefontsource/) que representa un archivo de fuente único. |
| [FONT_STREAM](#FONT-STREAM) | Un objeto [StreamFontSource](../../com.aspose.words/streamfontsource/) que representa un flujo con datos de fuentes. |
| [MEMORY_FONT](#MEMORY-FONT) | Un objeto [MemoryFontSource](../../com.aspose.words/memoryfontsource/) que representa una fuente única en memoria. |
| [SYSTEM_FONTS](#SYSTEM-FONTS) | Un objeto [SystemFontSource](../../com.aspose.words/systemfontsource/) que representa todas las fuentes instaladas en el sistema. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String fontSourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int fontSourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontSourceType)](#toString-int) |  |
### FONTS_FOLDER {#FONTS-FOLDER}
```
public static int FONTS_FOLDER
```


Un objeto [FolderFontSource](../../com.aspose.words/folderfontsource/) que representa una carpeta con archivos de fuentes.

### FONT_FILE {#FONT-FILE}
```
public static int FONT_FILE
```


Un objeto [FileFontSource](../../com.aspose.words/filefontsource/) que representa un archivo de fuente único.

### FONT_STREAM {#FONT-STREAM}
```
public static int FONT_STREAM
```


Un objeto [StreamFontSource](../../com.aspose.words/streamfontsource/) que representa un flujo con datos de fuentes.

### MEMORY_FONT {#MEMORY-FONT}
```
public static int MEMORY_FONT
```


Un objeto [MemoryFontSource](../../com.aspose.words/memoryfontsource/) que representa una fuente única en memoria.

### SYSTEM_FONTS {#SYSTEM-FONTS}
```
public static int SYSTEM_FONTS
```


Un objeto [SystemFontSource](../../com.aspose.words/systemfontsource/) que representa todas las fuentes instaladas en el sistema.

### length {#length}
```
public static int length
```


### fromName(String fontSourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String fontSourceTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fontSourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int fontSourceType) {#getName-int}
```
public static String getName(int fontSourceType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fontSourceType | int |  |

**Returns:**
java.lang.String
