---
title: "JustificationMode"
linktitle: "JustificationMode"
second_title: "Aspose.Words pour Java"
description: "Spécifie le réglage de l’espacement des caractères pour un document en Java."
type: docs
weight: 411
url: /fr/java/com.aspose.words/justificationmode/
---

**Inheritance:**
java.lang.Object
```
public class JustificationMode
```

Spécifie le réglage de l’espacement des caractères pour un document. La valeur par défaut est  Expand .

 **Examples:** 

Montre comment gérer le contrôle de l’espacement des caractères.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 int justificationMode = doc.getJustificationMode();
 if (justificationMode == JustificationMode.EXPAND)
     doc.setJustificationMode(JustificationMode.COMPRESS);

 doc.save(getArtifactsDir() + "Document.SetJustificationMode.docx");
 
```
## Champs

| Champ | Description |
| --- | --- |
| [COMPRESS](#COMPRESS) | Compresser l’espacement des caractères. |
| [COMPRESS_KANA](#COMPRESS-KANA) | Compresser, en utilisant les règles des syllabaires kana, Hiragana et Katakana. |
| [EXPAND](#EXPAND) | Ne pas compresser l’espacement des caractères. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String justificationModeName)](#fromName-java.lang.String) |  |
| [getName(int justificationMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int justificationMode)](#toString-int) |  |
### COMPRESS {#COMPRESS}
```
public static int COMPRESS
```


Compresser l’espacement des caractères.

### COMPRESS_KANA {#COMPRESS-KANA}
```
public static int COMPRESS_KANA
```


Compresser, en utilisant les règles des syllabaires kana, Hiragana et Katakana.

### EXPAND {#EXPAND}
```
public static int EXPAND
```


Ne pas compresser l’espacement des caractères.

### length {#length}
```
public static int length
```


### fromName(String justificationModeName) {#fromName-java.lang.String}
```
public static int fromName(String justificationModeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| justificationModeName | java.lang.String |  |

**Returns:**
int
### getName(int justificationMode) {#getName-int}
```
public static String getName(int justificationMode)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| justificationMode | int |  |

**Returns:**
java.lang.String
