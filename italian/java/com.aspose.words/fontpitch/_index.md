---
title: "FontPitch"
linktitle: "FontPitch"
second_title: "Aspose.Words per Java"
description: "Rappresenta la spaziatura del carattere in Java."
type: docs
weight: 330
url: /it/java/com.aspose.words/fontpitch/
---

**Inheritance:**
java.lang.Object
```
public class FontPitch
```

Rappresenta la larghezza del font.

 **Remarks:** 

Il pitch indica se il font è a larghezza fissa, a spaziatura proporzionale o si basa su un'impostazione predefinita.

 **Examples:** 

Mostra come accedere e stampare i dettagli di ogni carattere in un documento.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [DEFAULT](#DEFAULT) | Specifica che non sono disponibili informazioni sulla spaziatura di un carattere. |
| [FIXED](#FIXED) | Specifica che questo è un carattere a larghezza fissa. |
| [VARIABLE](#VARIABLE) | Specifica che questo è un carattere a larghezza proporzionale. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String fontPitchName)](#fromName-java.lang.String) |  |
| [getName(int fontPitch)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontPitch)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Specifica che non sono disponibili informazioni sulla spaziatura di un carattere.

### FIXED {#FIXED}
```
public static int FIXED
```


Specifica che questo è un carattere a larghezza fissa.

### VARIABLE {#VARIABLE}
```
public static int VARIABLE
```


Specifica che questo è un carattere a larghezza proporzionale.

### length {#length}
```
public static int length
```


### fromName(String fontPitchName) {#fromName-java.lang.String}
```
public static int fromName(String fontPitchName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontPitchName | java.lang.String |  |

**Returns:**
int
### getName(int fontPitch) {#getName-int}
```
public static String getName(int fontPitch)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontPitch | int |  |

**Returns:**
java.lang.String
