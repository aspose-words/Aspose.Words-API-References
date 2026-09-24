---
title: "FontPitch"
linktitle: "FontPitch"
second_title: "Aspose.Words para Java"
description: "Representa el pitch de la fuente en Java."
type: docs
weight: 330
url: /es/java/com.aspose.words/fontpitch/
---

**Inheritance:**
java.lang.Object
```
public class FontPitch
```

Representa el paso de la fuente.

 **Remarks:** 

El pitch indica si la fuente es de ancho fijo, espaciada proporcionalmente o depende de una configuración predeterminada.

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
| [DEFAULT](#DEFAULT) | Especifica que no hay información disponible sobre el pitch de una fuente. |
| [FIXED](#FIXED) | Especifica que esta es una fuente de ancho fijo. |
| [VARIABLE](#VARIABLE) | Especifica que esta es una fuente de ancho proporcional. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String fontPitchName)](#fromName-java.lang.String) |  |
| [getName(int fontPitch)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontPitch)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Especifica que no hay información disponible sobre el pitch de una fuente.

### FIXED {#FIXED}
```
public static int FIXED
```


Especifica que esta es una fuente de ancho fijo.

### VARIABLE {#VARIABLE}
```
public static int VARIABLE
```


Especifica que esta es una fuente de ancho proporcional.

### length {#length}
```
public static int length
```


### fromName(String fontPitchName) {#fromName-java.lang.String}
```
public static int fromName(String fontPitchName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fontPitchName | java.lang.String |  |

**Returns:**
int
### getName(int fontPitch) {#getName-int}
```
public static String getName(int fontPitch)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fontPitch | int |  |

**Returns:**
java.lang.String
