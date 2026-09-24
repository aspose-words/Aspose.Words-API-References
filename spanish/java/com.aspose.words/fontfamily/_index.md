---
title: "FontFamily"
linktitle: "FontFamily"
second_title: "Aspose.Words para Java"
description: "Representa la familia de fuentes en Java."
type: docs
weight: 324
url: /es/java/com.aspose.words/fontfamily/
---

**Inheritance:**
java.lang.Object
```
public class FontFamily
```

Representa la familia de fuentes.

 **Remarks:** 

Una familia de fuentes es un conjunto de tipografías que comparten ancho de trazo y características de serif.

 **Examples:** 

Muestra cómo acceder e imprimir los detalles de cada fuente en un documento.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [AUTO](#AUTO) | Especifica un nombre de familia genérico. |
| [DECORATIVE](#DECORATIVE) | Especifica una fuente novedosa. |
| [MODERN](#MODERN) | Especifica una fuente monoespaciada con o sin serifas. |
| [ROMAN](#ROMAN) | Especifica una fuente proporcional con serifas. |
| [SCRIPT](#SCRIPT) | Especifica una fuente diseñada para parecerse a la escritura a mano; ejemplos incluyen Script y Cursive. |
| [SWISS](#SWISS) | Especifica una fuente proporcional sin serifas. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String fontFamilyName)](#fromName-java.lang.String) |  |
| [getName(int fontFamily)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontFamily)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Especifica un nombre de familia genérico. Este nombre se usa cuando la información sobre una fuente no existe o no importa. Se usa la fuente predeterminada.

### DECORATIVE {#DECORATIVE}
```
public static int DECORATIVE
```


Especifica una fuente novedosa. Un ejemplo es Old English.

### MODERN {#MODERN}
```
public static int MODERN
```


Especifica una fuente monoespaciada con o sin serifas. Las fuentes monoespaciadas suelen ser modernas; ejemplos incluyen Pica, Elite y Courier New.

### ROMAN {#ROMAN}
```
public static int ROMAN
```


Especifica una fuente proporcional con serifas. Un ejemplo es Times New Roman.

### SCRIPT {#SCRIPT}
```
public static int SCRIPT
```


Especifica una fuente diseñada para parecerse a la escritura a mano; ejemplos incluyen Script y Cursive.

### SWISS {#SWISS}
```
public static int SWISS
```


Especifica una fuente proporcional sin serifas. Un ejemplo es Arial.

### length {#length}
```
public static int length
```


### fromName(String fontFamilyName) {#fromName-java.lang.String}
```
public static int fromName(String fontFamilyName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fontFamilyName | java.lang.String |  |

**Returns:**
int
### getName(int fontFamily) {#getName-int}
```
public static String getName(int fontFamily)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fontFamily | int |  |

**Returns:**
java.lang.String
