---
title: FontFamily
linktitle: FontFamily
second_title: Aspose.Words for Java
description: Represents the font family in Java.
type: docs
weight: 314
url: /java/com.aspose.words/fontfamily/
---

**Inheritance:**
java.lang.Object
```
public class FontFamily
```

Represents the font family.

 **Remarks:** 

A font family is a set of fonts having common stroke width and serif characteristics.

 **Examples:** 

Shows how to access and print details of each font in a document.

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
## Fields

| Field | Description |
| --- | --- |
| [AUTO](#AUTO) | Specifies a generic family name. |
| [DECORATIVE](#DECORATIVE) | Specifies a novelty font. |
| [MODERN](#MODERN) | Specifies a monospace font with or without serifs. |
| [ROMAN](#ROMAN) | Specifies a proportional font with serifs. |
| [SCRIPT](#SCRIPT) | Specifies a font that is designed to look like handwriting; examples include Script and Cursive. |
| [SWISS](#SWISS) | Specifies a proportional font without serifs. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String fontFamilyName)](#fromName-java.lang.String) |  |
| [getName(int fontFamily)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontFamily)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Specifies a generic family name. This name is used when information about a font does not exist or does not matter. The default font is used.

### DECORATIVE {#DECORATIVE}
```
public static int DECORATIVE
```


Specifies a novelty font. An example is Old English.

### MODERN {#MODERN}
```
public static int MODERN
```


Specifies a monospace font with or without serifs. Monospace fonts are usually modern; examples include Pica, Elite, and Courier New.

### ROMAN {#ROMAN}
```
public static int ROMAN
```


Specifies a proportional font with serifs. An example is Times New Roman.

### SCRIPT {#SCRIPT}
```
public static int SCRIPT
```


Specifies a font that is designed to look like handwriting; examples include Script and Cursive.

### SWISS {#SWISS}
```
public static int SWISS
```


Specifies a proportional font without serifs. An example is Arial.

### length {#length}
```
public static int length
```


### fromName(String fontFamilyName) {#fromName-java.lang.String}
```
public static int fromName(String fontFamilyName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontFamilyName | java.lang.String |  |

**Returns:**
int
### getName(int fontFamily) {#getName-int}
```
public static String getName(int fontFamily)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| fontFamily | int |  |

**Returns:**
java.lang.String
