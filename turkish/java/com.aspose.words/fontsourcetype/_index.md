---
title: "FontSourceType"
linktitle: "FontSourceType"
second_title: "Aspose.Words Java için"
description: "Java'da yazı tipi kaynağının türünü belirtir."
type: docs
weight: 334
url: /tr/java/com.aspose.words/fontsourcetype/
---

**Inheritance:**
java.lang.Object
```
public class FontSourceType
```

Yazı tipi kaynağının türünü belirtir.

 **Examples:** 

Yerel dosya sistemindeki bir yazı tipi dosyasını yazı tipi kaynağı olarak kullanmanın nasıl yapılacağını gösterir.

```

 FileFontSource fileFontSource = new FileFontSource(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{fileFontSource});

 Assert.assertEquals(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.getFilePath());
 Assert.assertEquals(FontSourceType.FONT_FILE, fileFontSource.getType());
 Assert.assertEquals(0, fileFontSource.getPriority());
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [FONTS_FOLDER](#FONTS-FOLDER) | Yazı tipi dosyalarını içeren klasörü temsil eden bir [FolderFontSource](../../com.aspose.words/folderfontsource/) nesnesi. |
| [FONT_FILE](#FONT-FILE) | Tek bir yazı tipi dosyasını temsil eden bir [FileFontSource](../../com.aspose.words/filefontsource/) nesnesi. |
| [FONT_STREAM](#FONT-STREAM) | Yazı tipi verileri içeren bir akışı temsil eden bir [StreamFontSource](../../com.aspose.words/streamfontsource/) nesnesi. |
| [MEMORY_FONT](#MEMORY-FONT) | Bellekte tek bir yazı tipini temsil eden bir [MemoryFontSource](../../com.aspose.words/memoryfontsource/) nesnesi. |
| [SYSTEM_FONTS](#SYSTEM-FONTS) | Sisteme yüklü tüm yazı tiplerini temsil eden bir [SystemFontSource](../../com.aspose.words/systemfontsource/) nesnesi. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String fontSourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int fontSourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontSourceType)](#toString-int) |  |
### FONTS_FOLDER {#FONTS-FOLDER}
```
public static int FONTS_FOLDER
```


Yazı tipi dosyalarını içeren klasörü temsil eden bir [FolderFontSource](../../com.aspose.words/folderfontsource/) nesnesi.

### FONT_FILE {#FONT-FILE}
```
public static int FONT_FILE
```


Tek bir yazı tipi dosyasını temsil eden bir [FileFontSource](../../com.aspose.words/filefontsource/) nesnesi.

### FONT_STREAM {#FONT-STREAM}
```
public static int FONT_STREAM
```


Yazı tipi verileri içeren bir akışı temsil eden bir [StreamFontSource](../../com.aspose.words/streamfontsource/) nesnesi.

### MEMORY_FONT {#MEMORY-FONT}
```
public static int MEMORY_FONT
```


Bellekte tek bir yazı tipini temsil eden bir [MemoryFontSource](../../com.aspose.words/memoryfontsource/) nesnesi.

### SYSTEM_FONTS {#SYSTEM-FONTS}
```
public static int SYSTEM_FONTS
```


Sisteme yüklü tüm yazı tiplerini temsil eden bir [SystemFontSource](../../com.aspose.words/systemfontsource/) nesnesi.

### length {#length}
```
public static int length
```


### fromName(String fontSourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String fontSourceTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontSourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int fontSourceType) {#getName-int}
```
public static String getName(int fontSourceType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontSourceType | int |  |

**Returns:**
java.lang.String
