---
title: TableAlignment
linktitle: TableAlignment
second_title: Aspose.Words for Java
description: Specifies alignment for an inline table in Java.
type: docs
weight: 569
url: /java/com.aspose.words/tablealignment/
---

**Inheritance:**
java.lang.Object
```
public class TableAlignment
```

Specifies alignment for an inline table.

 **Examples:** 

Shows how to apply an outline border to a table.

```

 Document doc = new Document(getMyDir() + "Tables.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Align the table to the center of the page.
 table.setAlignment(TableAlignment.CENTER);

 // Clear any existing borders and shading from the table.
 table.clearBorders();
 table.clearShading();

 // Add green borders to the outline of the table.
 table.setBorder(BorderType.LEFT, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.RIGHT, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.TOP, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.BOTTOM, LineStyle.SINGLE, 1.5, Color.GREEN, true);

 // Fill the cells with a light green solid color.
 table.setShading(TextureIndex.TEXTURE_SOLID, Color.GREEN, Color.GREEN);

 doc.save(getArtifactsDir() + "Table.SetOutlineBorders.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [CENTER](#CENTER) | The table is centered. |
| [LEFT](#LEFT) | The table is aligned to the left. |
| [RIGHT](#RIGHT) | The table is aligned to the right. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String tableAlignmentName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int tableAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int tableAlignment)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


The table is centered.

### LEFT {#LEFT}
```
public static int LEFT
```


The table is aligned to the left.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


The table is aligned to the right.

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
### fromName(String tableAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String tableAlignmentName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tableAlignmentName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int tableAlignment) {#getName-int}
```
public static String getName(int tableAlignment)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tableAlignment | int |  |

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
### toString(int tableAlignment) {#toString-int}
```
public static String toString(int tableAlignment)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tableAlignment | int |  |

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

