---
title: "FontFamily"
linktitle: "FontFamily"
second_title: "Aspose.Words pour Java"
description: "Représente la famille de polices en Java."
type: docs
weight: 324
url: /fr/java/com.aspose.words/fontfamily/
---

**Inheritance:**
java.lang.Object
```
public class FontFamily
```

Représente la famille de police.

 **Remarks:** 

Une famille de polices est un ensemble de polices ayant une largeur de trait et des caractéristiques de serif communes.

 **Examples:** 

Montre comment accéder et imprimer les détails de chaque police dans un document.

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
## Champs

| Champ | Description |
| --- | --- |
| [AUTO](#AUTO) | Spécifie un nom de famille générique. |
| [DECORATIVE](#DECORATIVE) | Spécifie une police fantaisie. |
| [MODERN](#MODERN) | Spécifie une police à chasse fixe avec ou sans empattements. |
| [ROMAN](#ROMAN) | Spécifie une police proportionnelle avec empattements. |
| [SCRIPT](#SCRIPT) | Spécifie une police conçue pour ressembler à une écriture manuscrite ; des exemples incluent Script et Cursive. |
| [SWISS](#SWISS) | Spécifie une police proportionnelle sans empattements. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String fontFamilyName)](#fromName-java.lang.String) |  |
| [getName(int fontFamily)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontFamily)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Spécifie un nom de famille générique. Ce nom est utilisé lorsque les informations sur une police n'existent pas ou ne sont pas importantes. La police par défaut est utilisée.

### DECORATIVE {#DECORATIVE}
```
public static int DECORATIVE
```


Spécifie une police fantaisie. Un exemple est Old English.

### MODERN {#MODERN}
```
public static int MODERN
```


Spécifie une police à chasse fixe avec ou sans empattements. Les polices à chasse fixe sont généralement modernes ; des exemples incluent Pica, Elite et Courier New.

### ROMAN {#ROMAN}
```
public static int ROMAN
```


Spécifie une police proportionnelle avec empattements. Un exemple est Times New Roman.

### SCRIPT {#SCRIPT}
```
public static int SCRIPT
```


Spécifie une police conçue pour ressembler à une écriture manuscrite ; des exemples incluent Script et Cursive.

### SWISS {#SWISS}
```
public static int SWISS
```


Spécifie une police proportionnelle sans empattements. Un exemple est Arial.

### length {#length}
```
public static int length
```


### fromName(String fontFamilyName) {#fromName-java.lang.String}
```
public static int fromName(String fontFamilyName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| fontFamilyName | java.lang.String |  |

**Returns:**
int
### getName(int fontFamily) {#getName-int}
```
public static String getName(int fontFamily)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| fontFamily | int |  |

**Returns:**
java.lang.String
