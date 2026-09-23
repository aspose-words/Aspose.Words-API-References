---
title: "JustificationMode"
linktitle: "JustificationMode"
second_title: "Aspose.Words per Java"
description: "Specifica la regolazione della spaziatura dei caratteri per un documento in Java."
type: docs
weight: 411
url: /it/java/com.aspose.words/justificationmode/
---

**Inheritance:**
java.lang.Object
```
public class JustificationMode
```

Specifica la regolazione della spaziatura dei caratteri per un documento. Il valore predefinito è  Expand .

 **Examples:** 

Mostra come gestire il controllo della spaziatura dei caratteri.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 int justificationMode = doc.getJustificationMode();
 if (justificationMode == JustificationMode.EXPAND)
     doc.setJustificationMode(JustificationMode.COMPRESS);

 doc.save(getArtifactsDir() + "Document.SetJustificationMode.docx");
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [COMPRESS](#COMPRESS) | Comprimi la spaziatura dei caratteri. |
| [COMPRESS_KANA](#COMPRESS-KANA) | Comprimi, usando le regole delle sillabari kana, Hiragana e Katakana. |
| [EXPAND](#EXPAND) | Non comprimere la spaziatura dei caratteri. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String justificationModeName)](#fromName-java.lang.String) |  |
| [getName(int justificationMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int justificationMode)](#toString-int) |  |
### COMPRESS {#COMPRESS}
```
public static int COMPRESS
```


Comprimi la spaziatura dei caratteri.

### COMPRESS_KANA {#COMPRESS-KANA}
```
public static int COMPRESS_KANA
```


Comprimi, usando le regole delle sillabari kana, Hiragana e Katakana.

### EXPAND {#EXPAND}
```
public static int EXPAND
```


Non comprimere la spaziatura dei caratteri.

### length {#length}
```
public static int length
```


### fromName(String justificationModeName) {#fromName-java.lang.String}
```
public static int fromName(String justificationModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| justificationModeName | java.lang.String |  |

**Returns:**
int
### getName(int justificationMode) {#getName-int}
```
public static String getName(int justificationMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| justificationMode | int |  |

**Returns:**
java.lang.String
