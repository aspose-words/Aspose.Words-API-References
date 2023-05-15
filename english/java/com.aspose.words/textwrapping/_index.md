---
title: TextWrapping
linktitle: TextWrapping
second_title: Aspose.Words for Java
description: Specifies how text is wrapped around the table in Java.
type: docs
weight: 590
url: /java/com.aspose.words/textwrapping/
---

**Inheritance:**
java.lang.Object
```
public class TextWrapping
```

Specifies how text is wrapped around the table.

 **Examples:** 

Shows how to work with table text wrapping.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 builder.getFont().setSize(16.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 // Set the "TextWrapping" property to "TextWrapping.Around" to get the table to wrap text around it,
 // and push it down into the paragraph below by setting the position.
 table.setTextWrapping(TextWrapping.AROUND);
 table.setAbsoluteHorizontalDistance(100.0);
 table.setAbsoluteVerticalDistance(20.0);

 doc.save(getArtifactsDir() + "Table.WrapText.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [AROUND](#AROUND) | Text is wrapped around the table occupying available side space. |
| [DEFAULT](#DEFAULT) | Default value. |
| [NONE](#NONE) | Text and table is displayed in the order of their appearance in the document. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String textWrappingName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int textWrapping)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int textWrapping)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### AROUND {#AROUND}
```
public static int AROUND
```


Text is wrapped around the table occupying available side space.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Default value.

### NONE {#NONE}
```
public static int NONE
```


Text and table is displayed in the order of their appearance in the document.

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
### fromName(String textWrappingName) {#fromName-java.lang.String}
```
public static int fromName(String textWrappingName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| textWrappingName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int textWrapping) {#getName-int}
```
public static String getName(int textWrapping)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| textWrapping | int |  |

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
### toString(int textWrapping) {#toString-int}
```
public static String toString(int textWrapping)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| textWrapping | int |  |

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

