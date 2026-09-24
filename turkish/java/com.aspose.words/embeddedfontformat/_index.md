---
title: "EmbeddedFontFormat"
linktitle: "EmbeddedFontFormat"
second_title: "Aspose.Words Java için"
description: "Java'daki FontInfo nesnesi içinde belirli gömülü yazı tipinin biçimini belirtir."
type: docs
weight: 184
url: /tr/java/com.aspose.words/embeddedfontformat/
---

**Inheritance:**
java.lang.Object
```
public class EmbeddedFontFormat
```

Belirli bir gömülü yazı tipinin biçimini [FontInfo](../../com.aspose.words/fontinfo/) nesnesi içinde belirtir.

Bir belge bir dosyaya kaydedildiğinde, yalnızca ilgili biçimdeki gömülü yazı tipleri yazılır.

 **Examples:** 

Gömülü bir yazı tipinin bir belgeden nasıl çıkarılacağını ve yerel dosya sistemine nasıl kaydedileceğini gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [EMBEDDED_OPEN_TYPE](#EMBEDDED-OPEN-TYPE) | Gömülü OpenType (EOT) Dosya Biçimini belirtir. |
| [OPEN_TYPE](#OPEN-TYPE) | OpenType (TrueType) yazı tipi dosyasının sade bir kopyası olarak gömülen yazı tipini belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String embeddedFontFormatName)](#fromName-java.lang.String) |  |
| [getName(int embeddedFontFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int embeddedFontFormat)](#toString-int) |  |
### EMBEDDED_OPEN_TYPE {#EMBEDDED-OPEN-TYPE}
```
public static int EMBEDDED_OPEN_TYPE
```


Gömülü OpenType (EOT) Dosya Biçimini belirtir.

Bu gömülü yazı tipi biçimi DOC dosyalarında kullanılır.

 **Remarks:** 

Biçimin açıklaması için http://www.w3.org/Submission/EOT adresine bakın.

### OPEN_TYPE {#OPEN-TYPE}
```
public static int OPEN_TYPE
```


OpenType (TrueType) yazı tipi dosyasının sade bir kopyası olarak gömülen yazı tipini belirtir.

Bu gömülü yazı tipi biçimi, DOCX dosyaları dahil Open Office XML formatında kullanılır.

### length {#length}
```
public static int length
```


### fromName(String embeddedFontFormatName) {#fromName-java.lang.String}
```
public static int fromName(String embeddedFontFormatName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| embeddedFontFormatName | java.lang.String |  |

**Returns:**
int
### getName(int embeddedFontFormat) {#getName-int}
```
public static String getName(int embeddedFontFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| embeddedFontFormat | int |  |

**Returns:**
java.lang.String
