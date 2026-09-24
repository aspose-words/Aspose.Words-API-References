---
title: "JustificationMode"
linktitle: "JustificationMode"
second_title: "Aspose.Words para Java"
description: "Especifica el ajuste del espaciado de caracteres para un documento en Java."
type: docs
weight: 411
url: /es/java/com.aspose.words/justificationmode/
---

**Inheritance:**
java.lang.Object
```
public class JustificationMode
```

Especifica el ajuste del espaciado de caracteres para un documento. El valor predeterminado es  Expand .

 **Examples:** 

Muestra cómo gestionar el control del espaciado de caracteres.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 int justificationMode = doc.getJustificationMode();
 if (justificationMode == JustificationMode.EXPAND)
     doc.setJustificationMode(JustificationMode.COMPRESS);

 doc.save(getArtifactsDir() + "Document.SetJustificationMode.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [COMPRESS](#COMPRESS) | Comprimir el espaciado de caracteres. |
| [COMPRESS_KANA](#COMPRESS-KANA) | Comprimir, usando las reglas de los silabarios kana, Hiragana y Katakana. |
| [EXPAND](#EXPAND) | No comprimir el espaciado de caracteres. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String justificationModeName)](#fromName-java.lang.String) |  |
| [getName(int justificationMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int justificationMode)](#toString-int) |  |
### COMPRESS {#COMPRESS}
```
public static int COMPRESS
```


Comprimir el espaciado de caracteres.

### COMPRESS_KANA {#COMPRESS-KANA}
```
public static int COMPRESS_KANA
```


Comprimir, usando las reglas de los silabarios kana, Hiragana y Katakana.

### EXPAND {#EXPAND}
```
public static int EXPAND
```


No comprimir el espaciado de caracteres.

### length {#length}
```
public static int length
```


### fromName(String justificationModeName) {#fromName-java.lang.String}
```
public static int fromName(String justificationModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| justificationModeName | java.lang.String |  |

**Returns:**
int
### getName(int justificationMode) {#getName-int}
```
public static String getName(int justificationMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| justificationMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int justificationMode) {#toString-int}
```
public static String toString(int justificationMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| justificationMode | int |  |

**Returns:**
java.lang.String
