---
title: "FontSourceType"
linktitle: "FontSourceType"
second_title: "Aspose.Words pour Java"
description: "Spécifie le type de source de police en Java."
type: docs
weight: 334
url: /fr/java/com.aspose.words/fontsourcetype/
---

**Inheritance:**
java.lang.Object
```
public class FontSourceType
```

Spécifie le type de source de police.

 **Examples:** 

Montre comment utiliser un fichier de police du système de fichiers local comme source de police.

```

 FileFontSource fileFontSource = new FileFontSource(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{fileFontSource});

 Assert.assertEquals(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.getFilePath());
 Assert.assertEquals(FontSourceType.FONT_FILE, fileFontSource.getType());
 Assert.assertEquals(0, fileFontSource.getPriority());
 
```
## Champs

| Champ | Description |
| --- | --- |
| [FONTS_FOLDER](#FONTS-FOLDER) | Un objet [FolderFontSource](../../com.aspose.words/folderfontsource/) qui représente un dossier contenant des fichiers de police. |
| [FONT_FILE](#FONT-FILE) | Un objet [FileFontSource](../../com.aspose.words/filefontsource/) qui représente un fichier de police unique. |
| [FONT_STREAM](#FONT-STREAM) | Un objet [StreamFontSource](../../com.aspose.words/streamfontsource/) qui représente un flux contenant des données de police. |
| [MEMORY_FONT](#MEMORY-FONT) | Un objet [MemoryFontSource](../../com.aspose.words/memoryfontsource/) qui représente une police unique en mémoire. |
| [SYSTEM_FONTS](#SYSTEM-FONTS) | Un objet [SystemFontSource](../../com.aspose.words/systemfontsource/) qui représente toutes les polices installées sur le système. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String fontSourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int fontSourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontSourceType)](#toString-int) |  |
### FONTS_FOLDER {#FONTS-FOLDER}
```
public static int FONTS_FOLDER
```


Un objet [FolderFontSource](../../com.aspose.words/folderfontsource/) qui représente un dossier contenant des fichiers de police.

### FONT_FILE {#FONT-FILE}
```
public static int FONT_FILE
```


Un objet [FileFontSource](../../com.aspose.words/filefontsource/) qui représente un fichier de police unique.

### FONT_STREAM {#FONT-STREAM}
```
public static int FONT_STREAM
```


Un objet [StreamFontSource](../../com.aspose.words/streamfontsource/) qui représente un flux contenant des données de police.

### MEMORY_FONT {#MEMORY-FONT}
```
public static int MEMORY_FONT
```


Un objet [MemoryFontSource](../../com.aspose.words/memoryfontsource/) qui représente une police unique en mémoire.

### SYSTEM_FONTS {#SYSTEM-FONTS}
```
public static int SYSTEM_FONTS
```


Un objet [SystemFontSource](../../com.aspose.words/systemfontsource/) qui représente toutes les polices installées sur le système.

### length {#length}
```
public static int length
```


### fromName(String fontSourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String fontSourceTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| fontSourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int fontSourceType) {#getName-int}
```
public static String getName(int fontSourceType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| fontSourceType | int |  |

**Returns:**
java.lang.String
