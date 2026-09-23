---
title: "FontFamily"
linktitle: "FontFamily"
second_title: "Aspose.Words per Java"
description: "Rappresenta la famiglia di caratteri in Java."
type: docs
weight: 324
url: /it/java/com.aspose.words/fontfamily/
---

**Inheritance:**
java.lang.Object
```
public class FontFamily
```

Rappresenta la famiglia del font.

 **Remarks:** 

Una famiglia di caratteri è un insieme di font con larghezza di tratto e caratteristiche di grazie comuni.

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
| [AUTO](#AUTO) | Specifica un nome di famiglia generico. |
| [DECORATIVE](#DECORATIVE) | Specifica un carattere decorativo. |
| [MODERN](#MODERN) | Specifica un carattere monospazio con o senza grazie. |
| [ROMAN](#ROMAN) | Specifica un carattere proporzionale con grazie. |
| [SCRIPT](#SCRIPT) | Specifica un carattere progettato per assomigliare alla scrittura a mano; esempi includono Script e Cursive. |
| [SWISS](#SWISS) | Specifica un carattere proporzionale senza grazie. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String fontFamilyName)](#fromName-java.lang.String) |  |
| [getName(int fontFamily)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontFamily)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Specifica un nome di famiglia generico. Questo nome è usato quando le informazioni su un carattere non esistono o non sono rilevanti. Viene usato il carattere predefinito.

### DECORATIVE {#DECORATIVE}
```
public static int DECORATIVE
```


Specifica un carattere decorativo. Un esempio è Old English.

### MODERN {#MODERN}
```
public static int MODERN
```


Specifica un carattere monospazio con o senza grazie. I caratteri monospazio sono solitamente moderni; esempi includono Pica, Elite e Courier New.

### ROMAN {#ROMAN}
```
public static int ROMAN
```


Specifica un carattere proporzionale con grazie. Un esempio è Times New Roman.

### SCRIPT {#SCRIPT}
```
public static int SCRIPT
```


Specifica un carattere progettato per assomigliare alla scrittura a mano; esempi includono Script e Cursive.

### SWISS {#SWISS}
```
public static int SWISS
```


Specifica un carattere proporzionale senza grazie. Un esempio è Arial.

### length {#length}
```
public static int length
```


### fromName(String fontFamilyName) {#fromName-java.lang.String}
```
public static int fromName(String fontFamilyName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontFamilyName | java.lang.String |  |

**Returns:**
int
### getName(int fontFamily) {#getName-int}
```
public static String getName(int fontFamily)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontFamily | int |  |

**Returns:**
java.lang.String
