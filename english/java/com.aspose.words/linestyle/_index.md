---
title: LineStyle
linktitle: LineStyle
second_title: Aspose.Words for Java
description: Specifies line style of a Border in Java.
type: docs
weight: 406
url: /java/com.aspose.words/linestyle/
---

**Inheritance:**
java.lang.Object
```
public class LineStyle
```

Specifies line style of a [Border](../../com.aspose.words/border/).

 **Examples:** 

Shows how to insert a string surrounded by a border into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [DASH_DOT_STROKER](#DASH-DOT-STROKER) |  |
| [DASH_LARGE_GAP](#DASH-LARGE-GAP) |  |
| [DASH_SMALL_GAP](#DASH-SMALL-GAP) |  |
| [DOT](#DOT) |  |
| [DOT_DASH](#DOT-DASH) |  |
| [DOT_DOT_DASH](#DOT-DOT-DASH) |  |
| [DOUBLE](#DOUBLE) |  |
| [DOUBLE_WAVE](#DOUBLE-WAVE) |  |
| [EMBOSS_3_D](#EMBOSS-3-D) |  |
| [ENGRAVE_3_D](#ENGRAVE-3-D) |  |
| [HAIRLINE](#HAIRLINE) |  |
| [INSET](#INSET) |  |
| [NONE](#NONE) |  |
| [OUTSET](#OUTSET) |  |
| [SINGLE](#SINGLE) |  |
| [THICK](#THICK) |  |
| [THICK_THIN_LARGE_GAP](#THICK-THIN-LARGE-GAP) |  |
| [THICK_THIN_MEDIUM_GAP](#THICK-THIN-MEDIUM-GAP) |  |
| [THICK_THIN_SMALL_GAP](#THICK-THIN-SMALL-GAP) |  |
| [THIN_THICK_LARGE_GAP](#THIN-THICK-LARGE-GAP) |  |
| [THIN_THICK_MEDIUM_GAP](#THIN-THICK-MEDIUM-GAP) |  |
| [THIN_THICK_SMALL_GAP](#THIN-THICK-SMALL-GAP) |  |
| [THIN_THICK_THIN_LARGE_GAP](#THIN-THICK-THIN-LARGE-GAP) |  |
| [THIN_THICK_THIN_MEDIUM_GAP](#THIN-THICK-THIN-MEDIUM-GAP) |  |
| [THIN_THICK_THIN_SMALL_GAP](#THIN-THICK-THIN-SMALL-GAP) |  |
| [TRIPLE](#TRIPLE) |  |
| [WAVE](#WAVE) |  |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String lineStyleName)](#fromName-java.lang.String) |  |
| [getName(int lineStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int lineStyle)](#toString-int) |  |
### DASH_DOT_STROKER {#DASH-DOT-STROKER}
```
public static int DASH_DOT_STROKER
```




### DASH_LARGE_GAP {#DASH-LARGE-GAP}
```
public static int DASH_LARGE_GAP
```




### DASH_SMALL_GAP {#DASH-SMALL-GAP}
```
public static int DASH_SMALL_GAP
```




### DOT {#DOT}
```
public static int DOT
```




### DOT_DASH {#DOT-DASH}
```
public static int DOT_DASH
```




### DOT_DOT_DASH {#DOT-DOT-DASH}
```
public static int DOT_DOT_DASH
```




### DOUBLE {#DOUBLE}
```
public static int DOUBLE
```




### DOUBLE_WAVE {#DOUBLE-WAVE}
```
public static int DOUBLE_WAVE
```




### EMBOSS_3_D {#EMBOSS-3-D}
```
public static int EMBOSS_3_D
```




### ENGRAVE_3_D {#ENGRAVE-3-D}
```
public static int ENGRAVE_3_D
```




### HAIRLINE {#HAIRLINE}
```
public static int HAIRLINE
```




### INSET {#INSET}
```
public static int INSET
```




### NONE {#NONE}
```
public static int NONE
```




### OUTSET {#OUTSET}
```
public static int OUTSET
```




### SINGLE {#SINGLE}
```
public static int SINGLE
```




### THICK {#THICK}
```
public static int THICK
```




### THICK_THIN_LARGE_GAP {#THICK-THIN-LARGE-GAP}
```
public static int THICK_THIN_LARGE_GAP
```




### THICK_THIN_MEDIUM_GAP {#THICK-THIN-MEDIUM-GAP}
```
public static int THICK_THIN_MEDIUM_GAP
```




### THICK_THIN_SMALL_GAP {#THICK-THIN-SMALL-GAP}
```
public static int THICK_THIN_SMALL_GAP
```




### THIN_THICK_LARGE_GAP {#THIN-THICK-LARGE-GAP}
```
public static int THIN_THICK_LARGE_GAP
```




### THIN_THICK_MEDIUM_GAP {#THIN-THICK-MEDIUM-GAP}
```
public static int THIN_THICK_MEDIUM_GAP
```




### THIN_THICK_SMALL_GAP {#THIN-THICK-SMALL-GAP}
```
public static int THIN_THICK_SMALL_GAP
```




### THIN_THICK_THIN_LARGE_GAP {#THIN-THICK-THIN-LARGE-GAP}
```
public static int THIN_THICK_THIN_LARGE_GAP
```




### THIN_THICK_THIN_MEDIUM_GAP {#THIN-THICK-THIN-MEDIUM-GAP}
```
public static int THIN_THICK_THIN_MEDIUM_GAP
```




### THIN_THICK_THIN_SMALL_GAP {#THIN-THICK-THIN-SMALL-GAP}
```
public static int THIN_THICK_THIN_SMALL_GAP
```




### TRIPLE {#TRIPLE}
```
public static int TRIPLE
```




### WAVE {#WAVE}
```
public static int WAVE
```




### length {#length}
```
public static int length
```


### fromName(String lineStyleName) {#fromName-java.lang.String}
```
public static int fromName(String lineStyleName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| lineStyleName | java.lang.String |  |

**Returns:**
int
### getName(int lineStyle) {#getName-int}
```
public static String getName(int lineStyle)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| lineStyle | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int lineStyle) {#toString-int}
```
public static String toString(int lineStyle)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| lineStyle | int |  |

**Returns:**
java.lang.String
