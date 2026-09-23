---
title: "BaselineAlignment"
linktitle: "BaselineAlignment"
second_title: "Aspose.Words per Java"
description: "Specifica la posizione verticale dei caratteri su una riga in Java."
type: docs
weight: 36
url: /it/java/com.aspose.words/baselinealignment/
---

**Inheritance:**
java.lang.Object
```
public class BaselineAlignment
```

Specifica la posizione verticale dei caratteri su una linea.

 **Examples:** 

Mostra come impostare la posizione verticale dei caratteri su una riga.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();
 if (format.getBaselineAlignment() == BaselineAlignment.AUTO)
 {
     format.setBaselineAlignment(BaselineAlignment.TOP);
 }

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphBaselineAlignment.docx");
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [AUTO](#AUTO) | La linea di base è regolata automaticamente. |
| [BASELINE](#BASELINE) | Allinea alla linea di base del paragrafo. |
| [BOTTOM](#BOTTOM) | Allinea al fondo di ogni carattere. |
| [CENTER](#CENTER) | Allinea i punti centrali di ogni carattere. |
| [TOP](#TOP) | Allinea lungo la parte superiore di ogni carattere. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String baselineAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int baselineAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int baselineAlignment)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


La linea di base è regolata automaticamente.

### BASELINE {#BASELINE}
```
public static int BASELINE
```


Allinea alla linea di base del paragrafo.

### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Allinea al fondo di ogni carattere.

### CENTER {#CENTER}
```
public static int CENTER
```


Allinea i punti centrali di ogni carattere.

### TOP {#TOP}
```
public static int TOP
```


Allinea lungo la parte superiore di ogni carattere.

### length {#length}
```
public static int length
```


### fromName(String baselineAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String baselineAlignmentName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| baselineAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int baselineAlignment) {#getName-int}
```
public static String getName(int baselineAlignment)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| baselineAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int baselineAlignment) {#toString-int}
```
public static String toString(int baselineAlignment)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| baselineAlignment | int |  |

**Returns:**
java.lang.String
