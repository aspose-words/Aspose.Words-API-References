---
title: "BaselineAlignment"
linktitle: "BaselineAlignment"
second_title: "Aspose.Words para Java"
description: "Especifica la posición vertical de las fuentes en una línea en Java."
type: docs
weight: 36
url: /es/java/com.aspose.words/baselinealignment/
---

**Inheritance:**
java.lang.Object
```
public class BaselineAlignment
```

Especifica la posición vertical de las fuentes en una línea.

 **Examples:** 

Muestra cómo establecer la posición vertical de las fuentes en una línea.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();
 if (format.getBaselineAlignment() == BaselineAlignment.AUTO)
 {
     format.setBaselineAlignment(BaselineAlignment.TOP);
 }

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphBaselineAlignment.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [AUTO](#AUTO) | La línea base se ajusta automáticamente. |
| [BASELINE](#BASELINE) | Se alinea a la línea base del párrafo. |
| [BOTTOM](#BOTTOM) | Se alinea al fondo de cada fuente. |
| [CENTER](#CENTER) | Alinea los puntos centrales de cada fuente. |
| [TOP](#TOP) | Se alinea a lo largo de la parte superior de cada fuente. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String baselineAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int baselineAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int baselineAlignment)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


La línea base se ajusta automáticamente.

### BASELINE {#BASELINE}
```
public static int BASELINE
```


Se alinea a la línea base del párrafo.

### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Se alinea al fondo de cada fuente.

### CENTER {#CENTER}
```
public static int CENTER
```


Alinea los puntos centrales de cada fuente.

### TOP {#TOP}
```
public static int TOP
```


Se alinea a lo largo de la parte superior de cada fuente.

### length {#length}
```
public static int length
```


### fromName(String baselineAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String baselineAlignmentName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| baselineAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int baselineAlignment) {#getName-int}
```
public static String getName(int baselineAlignment)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| baselineAlignment | int |  |

**Returns:**
java.lang.String
