---
title: TextOrientation
linktitle: TextOrientation
second_title: Aspose.Words for Java
description: Specifies orientation of text on a page in a table cell or a text frame in Java.
type: docs
weight: 586
url: /java/com.aspose.words/textorientation/
---

**Inheritance:**
java.lang.Object
```
public class TextOrientation
```

Specifies orientation of text on a page, in a table cell or a text frame.

 **Examples:** 

Shows how to build a formatted 2x2 table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [DOWNWARD](#DOWNWARD) | Text is rotated 90 degrees to the right to appear from top to bottom (tb-rl). |
| [HORIZONTAL](#HORIZONTAL) | Text is arranged horizontally (lr-tb). |
| [HORIZONTAL_ROTATED_FAR_EAST](#HORIZONTAL-ROTATED-FAR-EAST) | Text is arranged horizontally, but Far East characters are rotated 90 degrees to the left (lr-tb-v). |
| [UPWARD](#UPWARD) | Text is rotated 90 degrees to the left to appear from bottom to top (bt-lr). |
| [VERTICAL_FAR_EAST](#VERTICAL-FAR-EAST) | Far East characters appear vertical, other text is rotated 90 degrees to the right to appear from top to bottom (tb-rl-v). |
| [VERTICAL_ROTATED_FAR_EAST](#VERTICAL-ROTATED-FAR-EAST) | Far East characters appear vertical, other text is rotated 90 degrees to the right to appear from top to bottom vertically, then left to right horizontally (tb-lr-v). |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String textOrientationName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int textOrientation)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int textOrientation)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### DOWNWARD {#DOWNWARD}
```
public static int DOWNWARD
```


Text is rotated 90 degrees to the right to appear from top to bottom (tb-rl).

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Text is arranged horizontally (lr-tb).

### HORIZONTAL_ROTATED_FAR_EAST {#HORIZONTAL-ROTATED-FAR-EAST}
```
public static int HORIZONTAL_ROTATED_FAR_EAST
```


Text is arranged horizontally, but Far East characters are rotated 90 degrees to the left (lr-tb-v).

### UPWARD {#UPWARD}
```
public static int UPWARD
```


Text is rotated 90 degrees to the left to appear from bottom to top (bt-lr).

### VERTICAL_FAR_EAST {#VERTICAL-FAR-EAST}
```
public static int VERTICAL_FAR_EAST
```


Far East characters appear vertical, other text is rotated 90 degrees to the right to appear from top to bottom (tb-rl-v).

### VERTICAL_ROTATED_FAR_EAST {#VERTICAL-ROTATED-FAR-EAST}
```
public static int VERTICAL_ROTATED_FAR_EAST
```


Far East characters appear vertical, other text is rotated 90 degrees to the right to appear from top to bottom vertically, then left to right horizontally (tb-lr-v).

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### fromName(String textOrientationName) {#fromName-java.lang.String}
```
public static int fromName(String textOrientationName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| textOrientationName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int textOrientation) {#getName-int}
```
public static String getName(int textOrientation)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| textOrientation | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(int textOrientation) {#toString-int}
```
public static String toString(int textOrientation)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| textOrientation | int |  |

**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

