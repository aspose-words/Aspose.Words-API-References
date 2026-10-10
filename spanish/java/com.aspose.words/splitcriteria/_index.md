---
title: "SplitCriteria"
linktitle: "SplitCriteria"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se divide el documento en partes en Java."
type: docs
weight: 629
url: /es/java/com.aspose.words/splitcriteria/
---

**Inheritance:**
java.lang.Object
```
public class SplitCriteria
```

Especifica cómo se divide el documento en partes.

 **Examples:** 

Muestra cómo dividir el documento por páginas.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [PAGE](#PAGE) | Especifica que el documento se divide en páginas. |
| [SECTION_BREAK](#SECTION-BREAK) | Especifica que el documento se divide en partes en un salto de sección de cualquier tipo. |
| [STYLE](#STYLE) | Especifica que el documento se divide en partes en un párrafo formateado usando el estilo especificado en [SplitOptions.getSplitStyle()](../../com.aspose.words/splitoptions/\#getSplitStyle) / [SplitOptions.setSplitStyle(java.lang.String)](../../com.aspose.words/splitoptions/\#setSplitStyle-java.lang.String). |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String splitCriteriaName)](#fromName-java.lang.String) |  |
| [getName(int splitCriteria)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int splitCriteria)](#toString-int) |  |
### PAGE {#PAGE}
```
public static int PAGE
```


Especifica que el documento se divide en páginas.

### SECTION_BREAK {#SECTION-BREAK}
```
public static int SECTION_BREAK
```


Especifica que el documento se divide en partes en un salto de sección de cualquier tipo.

### STYLE {#STYLE}
```
public static int STYLE
```


Especifica que el documento se divide en partes en un párrafo formateado usando el estilo especificado en [SplitOptions.getSplitStyle()](../../com.aspose.words/splitoptions/\#getSplitStyle) / [SplitOptions.setSplitStyle(java.lang.String)](../../com.aspose.words/splitoptions/\#setSplitStyle-java.lang.String).

### length {#length}
```
public static int length
```


### fromName(String splitCriteriaName) {#fromName-java.lang.String}
```
public static int fromName(String splitCriteriaName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| splitCriteriaName | java.lang.String |  |

**Returns:**
int
### getName(int splitCriteria) {#getName-int}
```
public static String getName(int splitCriteria)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| splitCriteria | int |  |

**Returns:**
java.lang.String
