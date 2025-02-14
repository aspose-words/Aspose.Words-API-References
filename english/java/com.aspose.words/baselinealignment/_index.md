---
title: BaselineAlignment
linktitle: BaselineAlignment
second_title: Aspose.Words for Java
description: Specifies fonts vertical position on a line in Java.
type: docs
weight: 36
url: /java/com.aspose.words/baselinealignment/
---

**Inheritance:**
java.lang.Object
```
public class BaselineAlignment
```

Specifies fonts vertical position on a line.

 **Examples:** 

Shows how to set fonts vertical position on a line.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();
 if (format.getBaselineAlignment() == BaselineAlignment.AUTO)
 {
     format.setBaselineAlignment(BaselineAlignment.TOP);
 }

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphBaselineAlignment.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [AUTO](#AUTO) | Baseline is adjusted automatically. |
| [BASELINE](#BASELINE) | Aligns to the baseline of the paragraph. |
| [BOTTOM](#BOTTOM) | Aligns to the bottom of each font. |
| [CENTER](#CENTER) | Aligns the center points of each font. |
| [TOP](#TOP) | Aligns along the top of each font. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String baselineAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int baselineAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int baselineAlignment)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Baseline is adjusted automatically.

### BASELINE {#BASELINE}
```
public static int BASELINE
```


Aligns to the baseline of the paragraph.

### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Aligns to the bottom of each font.

### CENTER {#CENTER}
```
public static int CENTER
```


Aligns the center points of each font.

### TOP {#TOP}
```
public static int TOP
```


Aligns along the top of each font.

### length {#length}
```
public static int length
```


### fromName(String baselineAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String baselineAlignmentName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| baselineAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int baselineAlignment) {#getName-int}
```
public static String getName(int baselineAlignment)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| baselineAlignment | int |  |

**Returns:**
java.lang.String
