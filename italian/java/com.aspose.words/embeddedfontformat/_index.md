---
title: "EmbeddedFontFormat"
linktitle: "EmbeddedFontFormat"
second_title: "Aspose.Words per Java"
description: "Specifica il formato di un particolare font incorporato all'interno dell'oggetto FontInfo in Java."
type: docs
weight: 184
url: /it/java/com.aspose.words/embeddedfontformat/
---

**Inheritance:**
java.lang.Object
```
public class EmbeddedFontFormat
```

Specifica il formato di un particolare font incorporato all'interno dell'oggetto [FontInfo](../../com.aspose.words/fontinfo/).

Durante il salvataggio di un documento su file, vengono scritti solo i font incorporati del formato corrispondente.

 **Examples:** 

Mostra come estrarre un carattere incorporato da un documento e salvarlo nel file system locale.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [EMBEDDED_OPEN_TYPE](#EMBEDDED-OPEN-TYPE) | Specifica il formato di file Embedded OpenType (EOT). |
| [OPEN_TYPE](#OPEN-TYPE) | Specifica il font, incorporato come copia semplice del file di font OpenType (TrueType). |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String embeddedFontFormatName)](#fromName-java.lang.String) |  |
| [getName(int embeddedFontFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int embeddedFontFormat)](#toString-int) |  |
### EMBEDDED_OPEN_TYPE {#EMBEDDED-OPEN-TYPE}
```
public static int EMBEDDED_OPEN_TYPE
```


Specifica il formato di file Embedded OpenType (EOT).

Questo formato di font incorporati è usato nei file DOC.

 **Remarks:** 

Vedi http://www.w3.org/Submission/EOT per la descrizione del formato.

### OPEN_TYPE {#OPEN-TYPE}
```
public static int OPEN_TYPE
```


Specifica il font, incorporato come copia semplice del file di font OpenType (TrueType).

Questo formato di caratteri incorporati è utilizzato nel formato Open Office XML, inclusi i file DOCX.

### length {#length}
```
public static int length
```


### fromName(String embeddedFontFormatName) {#fromName-java.lang.String}
```
public static int fromName(String embeddedFontFormatName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| embeddedFontFormatName | java.lang.String |  |

**Returns:**
int
### getName(int embeddedFontFormat) {#getName-int}
```
public static String getName(int embeddedFontFormat)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| embeddedFontFormat | int |  |

**Returns:**
java.lang.String
