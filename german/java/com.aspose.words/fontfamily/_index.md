---
title: "FontFamily"
linktitle: "FontFamily"
second_title: "Aspose.Words für Java"
description: "Stellt die Schriftfamilie in Java dar."
type: docs
weight: 324
url: /de/java/com.aspose.words/fontfamily/
---

**Inheritance:**
java.lang.Object
```
public class FontFamily
```

Stellt die Schriftfamilie dar.

 **Remarks:** 

Eine Schriftfamilie ist eine Menge von Schriften mit gemeinsamer Strichstärke und Serifeneigenschaften.

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
| [AUTO](#AUTO) | Gibt einen generischen Familiennamen an. |
| [DECORATIVE](#DECORATIVE) | Gibt eine Neuheits-Schriftart an. |
| [MODERN](#MODERN) | Gibt eine Monospace-Schriftart mit oder ohne Serifen an. |
| [ROMAN](#ROMAN) | Gibt eine proportionale Schriftart mit Serifen an. |
| [SCRIPT](#SCRIPT) | Gibt eine Schriftart an, die wie Handschrift aussieht; Beispiele sind Script und Cursive. |
| [SWISS](#SWISS) | Gibt eine proportionale Schrift ohne Serifen an. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String fontFamilyName)](#fromName-java.lang.String) |  |
| [getName(int fontFamily)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontFamily)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Gibt einen generischen Familiennamen an. Dieser Name wird verwendet, wenn Informationen über eine Schriftart nicht vorhanden sind oder keine Rolle spielen. Die Standardschrift wird verwendet.

### DECORATIVE {#DECORATIVE}
```
public static int DECORATIVE
```


Gibt eine Sonderschrift an. Ein Beispiel ist Old English.

### MODERN {#MODERN}
```
public static int MODERN
```


Gibt eine Monospace-Schrift mit oder ohne Serifen an. Monospace-Schriften sind normalerweise modern; Beispiele sind Pica, Elite und Courier New.

### ROMAN {#ROMAN}
```
public static int ROMAN
```


Gibt eine proportionale Schrift mit Serifen an. Ein Beispiel ist Times New Roman.

### SCRIPT {#SCRIPT}
```
public static int SCRIPT
```


Gibt eine Schriftart an, die wie Handschrift aussieht; Beispiele sind Script und Cursive.

### SWISS {#SWISS}
```
public static int SWISS
```


Gibt eine proportionale Schrift ohne Serifen an. Ein Beispiel ist Arial.

### length {#length}
```
public static int length
```


### fromName(String fontFamilyName) {#fromName-java.lang.String}
```
public static int fromName(String fontFamilyName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontFamilyName | java.lang.String |  |

**Returns:**
int
### getName(int fontFamily) {#getName-int}
```
public static String getName(int fontFamily)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontFamily | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int fontFamily) {#toString-int}
```
public static String toString(int fontFamily)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontFamily | int |  |

**Returns:**
java.lang.String
