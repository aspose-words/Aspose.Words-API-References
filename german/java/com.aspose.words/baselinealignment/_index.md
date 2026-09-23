---
title: "BaselineAlignment"
linktitle: "BaselineAlignment"
second_title: "Aspose.Words für Java"
description: "Gibt die vertikale Position von Schriftarten in einer Zeile in Java an."
type: docs
weight: 36
url: /de/java/com.aspose.words/baselinealignment/
---

**Inheritance:**
java.lang.Object
```
public class BaselineAlignment
```

Gibt die vertikale Position von Schriftarten in einer Zeile an.

 **Examples:** 

Zeigt, wie die vertikale Position von Schriftarten in einer Zeile festgelegt wird.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();
 if (format.getBaselineAlignment() == BaselineAlignment.AUTO)
 {
     format.setBaselineAlignment(BaselineAlignment.TOP);
 }

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphBaselineAlignment.docx");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [AUTO](#AUTO) | Die Grundlinie wird automatisch angepasst. |
| [BASELINE](#BASELINE) | Richtet sich an der Grundlinie des Absatzes aus. |
| [BOTTOM](#BOTTOM) | Richtet sich am unteren Rand jeder Schriftart aus. |
| [CENTER](#CENTER) | Richtet die Mittelpunkte jeder Schriftart aus. |
| [TOP](#TOP) | Richtet sich entlang der Oberkante jeder Schriftart aus. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String baselineAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int baselineAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int baselineAlignment)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Die Grundlinie wird automatisch angepasst.

### BASELINE {#BASELINE}
```
public static int BASELINE
```


Richtet sich an der Grundlinie des Absatzes aus.

### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Richtet sich am unteren Rand jeder Schriftart aus.

### CENTER {#CENTER}
```
public static int CENTER
```


Richtet die Mittelpunkte jeder Schriftart aus.

### TOP {#TOP}
```
public static int TOP
```


Richtet sich entlang der Oberkante jeder Schriftart aus.

### length {#length}
```
public static int length
```


### fromName(String baselineAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String baselineAlignmentName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| baselineAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int baselineAlignment) {#getName-int}
```
public static String getName(int baselineAlignment)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| baselineAlignment | int |  |

**Returns:**
java.lang.String
