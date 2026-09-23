---
title: "EmbeddedFontFormat"
linktitle: "EmbeddedFontFormat"
second_title: "Aspose.Words für Java"
description: "Gibt das Format einer bestimmten eingebetteten Schriftart im FontInfo-Objekt in Java an."
type: docs
weight: 184
url: /de/java/com.aspose.words/embeddedfontformat/
---

**Inheritance:**
java.lang.Object
```
public class EmbeddedFontFormat
```

Gibt das Format einer bestimmten eingebetteten Schriftart im [FontInfo](../../com.aspose.words/fontinfo/)-Objekt an.

Beim Speichern eines Dokuments in einer Datei werden nur eingebettete Schriftarten des entsprechenden Formats geschrieben.

 **Examples:** 

Zeigt, wie eine eingebettete Schrift aus einem Dokument extrahiert und im lokalen Dateisystem gespeichert wird.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [EMBEDDED_OPEN_TYPE](#EMBEDDED-OPEN-TYPE) | Gibt das Embedded OpenType (EOT)-Dateiformat an. |
| [OPEN_TYPE](#OPEN-TYPE) | Gibt die Schriftart an, eingebettet als einfache Kopie einer OpenType (TrueType)-Schriftdatei. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String embeddedFontFormatName)](#fromName-java.lang.String) |  |
| [getName(int embeddedFontFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int embeddedFontFormat)](#toString-int) |  |
### EMBEDDED_OPEN_TYPE {#EMBEDDED-OPEN-TYPE}
```
public static int EMBEDDED_OPEN_TYPE
```


Gibt das Embedded OpenType (EOT)-Dateiformat an.

Dieses Format eingebetteter Schriftarten wird in DOC-Dateien verwendet.

 **Remarks:** 

Siehe http://www.w3.org/Submission/EOT für eine Beschreibung des Formats.

### OPEN_TYPE {#OPEN-TYPE}
```
public static int OPEN_TYPE
```


Gibt die Schriftart an, eingebettet als einfache Kopie einer OpenType (TrueType)-Schriftdatei.

Dieses Format eingebetteter Schriftarten wird im Open Office XML-Format verwendet, einschließlich DOCX-Dateien.

### length {#length}
```
public static int length
```


### fromName(String embeddedFontFormatName) {#fromName-java.lang.String}
```
public static int fromName(String embeddedFontFormatName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| embeddedFontFormatName | java.lang.String |  |

**Returns:**
int
### getName(int embeddedFontFormat) {#getName-int}
```
public static String getName(int embeddedFontFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| embeddedFontFormat | int |  |

**Returns:**
java.lang.String
