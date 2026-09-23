---
title: "FontPitch"
linktitle: "FontPitch"
second_title: "Aspose.Words für Java"
description: "Stellt die Schriftbreite in Java dar."
type: docs
weight: 330
url: /de/java/com.aspose.words/fontpitch/
---

**Inheritance:**
java.lang.Object
```
public class FontPitch
```

Stellt die Schriftbreite dar.

 **Remarks:** 

Die Zeichenbreite gibt an, ob die Schrift festbreit, proportional verteilt oder von einer Standardeinstellung abhängig ist.

 **Examples:** 

Zeigt, wie man auf jede Schrift in einem Dokument zugreift und deren Details ausgibt.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 Iterator fontCollectionEnumerator = doc.getFontInfos().iterator();
 while (fontCollectionEnumerator.hasNext()) {
     FontInfo fontInfo = fontCollectionEnumerator.next();
     if (fontInfo != null) {
         System.out.println("Font name: " + fontInfo.getName());

         // Alt names are usually blank.
         System.out.println("Alt name: " + fontInfo.getAltName());
         System.out.println("\t- Family: " + fontInfo.getFamily());
         System.out.println("\t- " + (fontInfo.isTrueType() ? "Is TrueType" : "Is not TrueType"));
         System.out.println("\t- Pitch: " + fontInfo.getPitch());
         System.out.println("\t- Charset: " + fontInfo.getCharset());
         System.out.println("\t- Panose:");
         System.out.println("\t\tFamily Kind: " + (fontInfo.getPanose()[0] & 0xFF));
         System.out.println("\t\tSerif Style: " + (fontInfo.getPanose()[1] & 0xFF));
         System.out.println("\t\tWeight: " + (fontInfo.getPanose()[2] & 0xFF));
         System.out.println("\t\tProportion: " + (fontInfo.getPanose()[3] & 0xFF));
         System.out.println("\t\tContrast: " + (fontInfo.getPanose()[4] & 0xFF));
         System.out.println("\t\tStroke Variation: " + (fontInfo.getPanose()[5] & 0xFF));
         System.out.println("\t\tArm Style: " + (fontInfo.getPanose()[6] & 0xFF));
         System.out.println("\t\tLetterform: " + (fontInfo.getPanose()[7] & 0xFF));
         System.out.println("\t\tMidline: " + (fontInfo.getPanose()[8] & 0xFF));
         System.out.println("\t\tX-Height: " + (fontInfo.getPanose()[9] & 0xFF));
     }
 }
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [DEFAULT](#DEFAULT) | Gibt an, dass keine Informationen über die Schriftbreite einer Schriftart verfügbar sind. |
| [FIXED](#FIXED) | Gibt an, dass es sich um eine Schrift mit fester Breite handelt. |
| [VARIABLE](#VARIABLE) | Gibt an, dass es sich um eine Schrift mit proportionaler Breite handelt. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String fontPitchName)](#fromName-java.lang.String) |  |
| [getName(int fontPitch)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontPitch)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Gibt an, dass keine Informationen über die Schriftbreite einer Schriftart verfügbar sind.

### FIXED {#FIXED}
```
public static int FIXED
```


Gibt an, dass es sich um eine Schrift mit fester Breite handelt.

### VARIABLE {#VARIABLE}
```
public static int VARIABLE
```


Gibt an, dass es sich um eine Schrift mit proportionaler Breite handelt.

### length {#length}
```
public static int length
```


### fromName(String fontPitchName) {#fromName-java.lang.String}
```
public static int fromName(String fontPitchName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontPitchName | java.lang.String |  |

**Returns:**
int
### getName(int fontPitch) {#getName-int}
```
public static String getName(int fontPitch)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontPitch | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int fontPitch) {#toString-int}
```
public static String toString(int fontPitch)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontPitch | int |  |

**Returns:**
java.lang.String
