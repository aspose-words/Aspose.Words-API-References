---
title: "BaselineAlignment"
linktitle: "BaselineAlignment"
second_title: "Aspose.Words pour Java"
description: "Spécifie la position verticale des polices sur une ligne en Java."
type: docs
weight: 36
url: /fr/java/com.aspose.words/baselinealignment/
---

**Inheritance:**
java.lang.Object
```
public class BaselineAlignment
```

Spécifie la position verticale des polices sur une ligne.

 **Examples:** 

Montre comment définir la position verticale des polices sur une ligne.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();
 if (format.getBaselineAlignment() == BaselineAlignment.AUTO)
 {
     format.setBaselineAlignment(BaselineAlignment.TOP);
 }

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphBaselineAlignment.docx");
 
```
## Champs

| Champ | Description |
| --- | --- |
| [AUTO](#AUTO) | La ligne de base est ajustée automatiquement. |
| [BASELINE](#BASELINE) | Aligne à la ligne de base du paragraphe. |
| [BOTTOM](#BOTTOM) | Aligne au bas de chaque police. |
| [CENTER](#CENTER) | Aligne les points centraux de chaque police. |
| [TOP](#TOP) | Aligne le long du haut de chaque police. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String baselineAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int baselineAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int baselineAlignment)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


La ligne de base est ajustée automatiquement.

### BASELINE {#BASELINE}
```
public static int BASELINE
```


Aligne à la ligne de base du paragraphe.

### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Aligne au bas de chaque police.

### CENTER {#CENTER}
```
public static int CENTER
```


Aligne les points centraux de chaque police.

### TOP {#TOP}
```
public static int TOP
```


Aligne le long du haut de chaque police.

### length {#length}
```
public static int length
```


### fromName(String baselineAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String baselineAlignmentName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| baselineAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int baselineAlignment) {#getName-int}
```
public static String getName(int baselineAlignment)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| baselineAlignment | int |  |

**Returns:**
java.lang.String
