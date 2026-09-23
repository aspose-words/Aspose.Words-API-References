---
title: "SplitCriteria"
linktitle: "SplitCriteria"
second_title: "Aspose.Words per Java"
description: "Specifica come il documento viene suddiviso in parti in Java."
type: docs
weight: 629
url: /it/java/com.aspose.words/splitcriteria/
---

**Inheritance:**
java.lang.Object
```
public class SplitCriteria
```

Specifica come il documento viene suddiviso in parti.

 **Examples:** 

Mostra come suddividere il documento per pagine.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [PAGE](#PAGE) | Specifica che il documento è suddiviso in pagine. |
| [SECTION_BREAK](#SECTION-BREAK) | Specifica che il documento è suddiviso in parti a una interruzione di sezione di qualsiasi tipo. |
| [STYLE](#STYLE) | Specifica che il documento è suddiviso in parti a un paragrafo formattato utilizzando lo stile specificato in [SplitOptions.getSplitStyle()](../../com.aspose.words/splitoptions/\#getSplitStyle) / [SplitOptions.setSplitStyle(java.lang.String)](../../com.aspose.words/splitoptions/\#setSplitStyle-java.lang.String). |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String splitCriteriaName)](#fromName-java.lang.String) |  |
| [getName(int splitCriteria)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int splitCriteria)](#toString-int) |  |
### PAGE {#PAGE}
```
public static int PAGE
```


Specifica che il documento è suddiviso in pagine.

### SECTION_BREAK {#SECTION-BREAK}
```
public static int SECTION_BREAK
```


Specifica che il documento è suddiviso in parti a una interruzione di sezione di qualsiasi tipo.

### STYLE {#STYLE}
```
public static int STYLE
```


Specifica che il documento è suddiviso in parti a un paragrafo formattato utilizzando lo stile specificato in [SplitOptions.getSplitStyle()](../../com.aspose.words/splitoptions/\#getSplitStyle) / [SplitOptions.setSplitStyle(java.lang.String)](../../com.aspose.words/splitoptions/\#setSplitStyle-java.lang.String).

### length {#length}
```
public static int length
```


### fromName(String splitCriteriaName) {#fromName-java.lang.String}
```
public static int fromName(String splitCriteriaName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| splitCriteriaName | java.lang.String |  |

**Returns:**
int
### getName(int splitCriteria) {#getName-int}
```
public static String getName(int splitCriteria)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| splitCriteria | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int splitCriteria) {#toString-int}
```
public static String toString(int splitCriteria)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| splitCriteria | int |  |

**Returns:**
java.lang.String
