---
title: "SplitCriteria"
linktitle: "SplitCriteria"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie das Dokument in Java in Teile aufgeteilt wird."
type: docs
weight: 629
url: /de/java/com.aspose.words/splitcriteria/
---

**Inheritance:**
java.lang.Object
```
public class SplitCriteria
```

Gibt an, wie das Dokument in Teile aufgeteilt wird.

 **Examples:** 

Zeigt, wie das Dokument nach Seiten aufgeteilt wird.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [PAGE](#PAGE) | Gibt an, dass das Dokument in Seiten aufgeteilt wird. |
| [SECTION_BREAK](#SECTION-BREAK) | Gibt an, dass das Dokument bei einem Abschnittswechsel beliebigen Typs in Teile aufgeteilt wird. |
| [STYLE](#STYLE) | Gibt an, dass das Dokument in Teile aufgeteilt wird bei einem Absatz, der mit dem in [SplitOptions.getSplitStyle()](../../com.aspose.words/splitoptions/\#getSplitStyle) / [SplitOptions.setSplitStyle(java.lang.String)](../../com.aspose.words/splitoptions/\#setSplitStyle-java.lang.String) angegebenen Stil formatiert ist. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String splitCriteriaName)](#fromName-java.lang.String) |  |
| [getName(int splitCriteria)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int splitCriteria)](#toString-int) |  |
### PAGE {#PAGE}
```
public static int PAGE
```


Gibt an, dass das Dokument in Seiten aufgeteilt wird.

### SECTION_BREAK {#SECTION-BREAK}
```
public static int SECTION_BREAK
```


Gibt an, dass das Dokument bei einem Abschnittswechsel beliebigen Typs in Teile aufgeteilt wird.

### STYLE {#STYLE}
```
public static int STYLE
```


Gibt an, dass das Dokument in Teile aufgeteilt wird bei einem Absatz, der mit dem in [SplitOptions.getSplitStyle()](../../com.aspose.words/splitoptions/\#getSplitStyle) / [SplitOptions.setSplitStyle(java.lang.String)](../../com.aspose.words/splitoptions/\#setSplitStyle-java.lang.String) angegebenen Stil formatiert ist.

### length {#length}
```
public static int length
```


### fromName(String splitCriteriaName) {#fromName-java.lang.String}
```
public static int fromName(String splitCriteriaName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| splitCriteriaName | java.lang.String |  |

**Returns:**
int
### getName(int splitCriteria) {#getName-int}
```
public static String getName(int splitCriteria)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| splitCriteria | int |  |

**Returns:**
java.lang.String
