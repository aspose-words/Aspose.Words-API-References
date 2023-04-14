---
title: DropCapPosition
linktitle: DropCapPosition
second_title: Aspose.Words for Java API Reference
description: Specifies the position for a drop cap text in Java.
type: docs
weight: 136
url: /java/com.aspose.words/dropcapposition/
---

**Inheritance:**
java.lang.Object
```
public class DropCapPosition
```

Specifies the position for a drop cap text.

 **Examples:** 

Shows how to create a drop cap.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert one paragraph with a large letter that the text in the second and third paragraphs begins with.
 builder.getFont().setSize(54.0);
 builder.writeln("L");

 builder.getFont().setSize(18.0);
 builder.writeln("orem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
 builder.writeln("Ut enim ad minim veniam, quis nostrud exercitation " +
         "ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 // Currently, the second and third paragraphs will appear underneath the first.
 // We can convert the first paragraph as a drop cap for the other paragraphs via its "ParagraphFormat" object.
 // Set the "DropCapPosition" property to "DropCapPosition.Margin" to place the drop cap
 // outside the left-hand side page margin if our text is left-to-right.
 // Set the "DropCapPosition" property to "DropCapPosition.Normal" to place the drop cap within the page margins
 // and to wrap the rest of the text around it.
 // "DropCapPosition.None" is the default state for all paragraphs.
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setDropCapPosition(dropCapPosition);

 doc.save(getArtifactsDir() + "ParagraphFormat.DropCap.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [MARGIN](#MARGIN) | The drop cap is positioned outside the text margin on the anchor paragraph. |
| [NONE](#NONE) | The paragraph does not have a drop cap. |
| [NORMAL](#NORMAL) | The drop cap is positioned inside the text margin on the anchor paragraph. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String dropCapPositionName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int dropCapPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int dropCapPosition)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### MARGIN {#MARGIN}
```
public static int MARGIN
```


The drop cap is positioned outside the text margin on the anchor paragraph.

### NONE {#NONE}
```
public static int NONE
```


The paragraph does not have a drop cap.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


The drop cap is positioned inside the text margin on the anchor paragraph.

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
### fromName(String dropCapPositionName) {#fromName-java.lang.String}
```
public static int fromName(String dropCapPositionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dropCapPositionName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int dropCapPosition) {#getName-int}
```
public static String getName(int dropCapPosition)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dropCapPosition | int |  |

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
### toString(int dropCapPosition) {#toString-int}
```
public static String toString(int dropCapPosition)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dropCapPosition | int |  |

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

