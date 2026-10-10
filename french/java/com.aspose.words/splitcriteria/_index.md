---
title: "SplitCriteria"
linktitle: "SplitCriteria"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment le document est divisé en parties en Java."
type: docs
weight: 629
url: /fr/java/com.aspose.words/splitcriteria/
---

**Inheritance:**
java.lang.Object
```
public class SplitCriteria
```

Spécifie comment le document est découpé en parties.

 **Examples:** 

Montre comment diviser le document par pages.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```
## Champs

| Champ | Description |
| --- | --- |
| [PAGE](#PAGE) | Spécifie que le document est divisé en pages. |
| [SECTION_BREAK](#SECTION-BREAK) | Spécifie que le document est divisé en parties à un saut de section de n'importe quel type. |
| [STYLE](#STYLE) | Spécifie que le document est divisé en parties à un paragraphe formaté en utilisant le style spécifié dans [SplitOptions.getSplitStyle()](../../com.aspose.words/splitoptions/\#getSplitStyle) / [SplitOptions.setSplitStyle(java.lang.String)](../../com.aspose.words/splitoptions/\#setSplitStyle-java.lang.String). |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String splitCriteriaName)](#fromName-java.lang.String) |  |
| [getName(int splitCriteria)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int splitCriteria)](#toString-int) |  |
### PAGE {#PAGE}
```
public static int PAGE
```


Spécifie que le document est divisé en pages.

### SECTION_BREAK {#SECTION-BREAK}
```
public static int SECTION_BREAK
```


Spécifie que le document est divisé en parties à un saut de section de n'importe quel type.

### STYLE {#STYLE}
```
public static int STYLE
```


Spécifie que le document est divisé en parties à un paragraphe formaté en utilisant le style spécifié dans [SplitOptions.getSplitStyle()](../../com.aspose.words/splitoptions/\#getSplitStyle) / [SplitOptions.setSplitStyle(java.lang.String)](../../com.aspose.words/splitoptions/\#setSplitStyle-java.lang.String).

### length {#length}
```
public static int length
```


### fromName(String splitCriteriaName) {#fromName-java.lang.String}
```
public static int fromName(String splitCriteriaName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| splitCriteriaName | java.lang.String |  |

**Returns:**
int
### getName(int splitCriteria) {#getName-int}
```
public static String getName(int splitCriteria)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| splitCriteria | int |  |

**Returns:**
java.lang.String
