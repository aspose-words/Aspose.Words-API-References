---
title: "EmphasisMark"
linktitle: "EmphasisMark"
second_title: "Aspose.Words per Java"
description: "Specifica i possibili tipi di segno di enfasi in Java."
type: docs
weight: 187
url: /it/java/com.aspose.words/emphasismark/
---

**Inheritance:**
java.lang.Object
```
public class EmphasisMark
```

Specifica i possibili tipi di segno di enfasi.

 **Examples:** 

Mostra come aggiungere un carattere aggiuntivo visualizzato sopra/sotto il glifo.

```

 DocumentBuilder builder = new DocumentBuilder();

 // Possible types of emphasis mark:
 // https://apireference.aspose.com/words/net/aspose.words/emphasismark
 builder.getFont().setEmphasisMark(emphasisMark);

 builder.write("Emphasis text");
 builder.writeln();
 builder.getFont().clearFormatting();
 builder.write("Simple text");

 builder.getDocument().save(getArtifactsDir() + "Fonts.SetEmphasisMark.docx");
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [NONE](#NONE) | Nessun segno di enfasi. |
| [OVER_COMMA](#OVER-COMMA) | Il segno di enfasi è un carattere virgola visualizzato sopra il testo. |
| [OVER_SOLID_CIRCLE](#OVER-SOLID-CIRCLE) | Il segno di enfasi è un cerchio nero pieno visualizzato sopra il testo. |
| [OVER_WHITE_CIRCLE](#OVER-WHITE-CIRCLE) | Il segno di enfasi è un cerchio bianco vuoto visualizzato sopra il testo. |
| [UNDER_SOLID_CIRCLE](#UNDER-SOLID-CIRCLE) | Il segno di enfasi è un cerchio nero pieno visualizzato sotto il testo. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String emphasisMarkName)](#fromName-java.lang.String) |  |
| [getName(int emphasisMark)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int emphasisMark)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Nessun segno di enfasi.

### OVER_COMMA {#OVER-COMMA}
```
public static int OVER_COMMA
```


Il segno di enfasi è un carattere virgola visualizzato sopra il testo.

### OVER_SOLID_CIRCLE {#OVER-SOLID-CIRCLE}
```
public static int OVER_SOLID_CIRCLE
```


Il segno di enfasi è un cerchio nero pieno visualizzato sopra il testo.

### OVER_WHITE_CIRCLE {#OVER-WHITE-CIRCLE}
```
public static int OVER_WHITE_CIRCLE
```


Il segno di enfasi è un cerchio bianco vuoto visualizzato sopra il testo.

### UNDER_SOLID_CIRCLE {#UNDER-SOLID-CIRCLE}
```
public static int UNDER_SOLID_CIRCLE
```


Il segno di enfasi è un cerchio nero pieno visualizzato sotto il testo.

### length {#length}
```
public static int length
```


### fromName(String emphasisMarkName) {#fromName-java.lang.String}
```
public static int fromName(String emphasisMarkName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| emphasisMarkName | java.lang.String |  |

**Returns:**
int
### getName(int emphasisMark) {#getName-int}
```
public static String getName(int emphasisMark)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| emphasisMark | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int emphasisMark) {#toString-int}
```
public static String toString(int emphasisMark)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| emphasisMark | int |  |

**Returns:**
java.lang.String
