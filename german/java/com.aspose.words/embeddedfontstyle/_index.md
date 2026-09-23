---
title: "EmbeddedFontStyle"
linktitle: "EmbeddedFontStyle"
second_title: "Aspose.Words für Java"
description: "Gibt den Stil einer eingebetteten Schriftart innerhalb eines FontInfo-Objekts in Java an."
type: docs
weight: 185
url: /de/java/com.aspose.words/embeddedfontstyle/
---

**Inheritance:**
java.lang.Object
```
public class EmbeddedFontStyle
```

Gibt den Stil einer eingebetteten Schriftart innerhalb eines [FontInfo](../../com.aspose.words/fontinfo/) Objekts an.

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
| [BOLD](#BOLD) | Gibt die fette eingebettete Schriftart an. |
| [BOLD_ITALIC](#BOLD-ITALIC) | Gibt die fette-kursive eingebettete Schriftart an. |
| [ITALIC](#ITALIC) | Gibt die kursive eingebettete Schriftart an. |
| [REGULAR](#REGULAR) | Gibt die normale eingebettete Schriftart an. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String embeddedFontStyleName)](#fromName-java.lang.String) |  |
| [fromNames(Set embeddedFontStyleNames)](#fromNames-java.util.Set) |  |
| [getName(int embeddedFontStyle)](#getName-int) |  |
| [getNames(int embeddedFontStyle)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int embeddedFontStyle)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### BOLD {#BOLD}
```
public static int BOLD
```


Gibt die fette eingebettete Schriftart an.

### BOLD_ITALIC {#BOLD-ITALIC}
```
public static int BOLD_ITALIC
```


Gibt die fette-kursive eingebettete Schriftart an.

### ITALIC {#ITALIC}
```
public static int ITALIC
```


Gibt die kursive eingebettete Schriftart an.

### REGULAR {#REGULAR}
```
public static int REGULAR
```


Gibt die normale eingebettete Schriftart an.

### length {#length}
```
public static int length
```


### fromName(String embeddedFontStyleName) {#fromName-java.lang.String}
```
public static int fromName(String embeddedFontStyleName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| embeddedFontStyleName | java.lang.String |  |

**Returns:**
int
### fromNames(Set embeddedFontStyleNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set embeddedFontStyleNames)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| embeddedFontStyleNames | java.util.Set |  |

**Returns:**
int
### getName(int embeddedFontStyle) {#getName-int}
```
public static String getName(int embeddedFontStyle)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| embeddedFontStyle | int |  |

**Returns:**
java.lang.String
### getNames(int embeddedFontStyle) {#getNames-int}
```
public static Set getNames(int embeddedFontStyle)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| embeddedFontStyle | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int embeddedFontStyle) {#toString-int}
```
public static String toString(int embeddedFontStyle)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| embeddedFontStyle | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
