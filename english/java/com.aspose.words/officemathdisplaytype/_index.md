---
title: OfficeMathDisplayType
linktitle: OfficeMathDisplayType
second_title: Aspose.Words for Java API Reference
description: Specifies the display format type of the equation in Java.
type: docs
weight: 428
url: /java/com.aspose.words/officemathdisplaytype/
---

**Inheritance:**
java.lang.Object
```
public class OfficeMathDisplayType
```

Specifies the display format type of the equation.

 **Examples:** 

Shows how to set office math display formatting.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);

 // OfficeMath nodes that are children of other OfficeMath nodes are always inline.
 // The node we are working with is the base node to change its location and display type.
 Assert.assertEquals(MathObjectType.O_MATH_PARA, officeMath.getMathObjectType());
 Assert.assertEquals(NodeType.OFFICE_MATH, officeMath.getNodeType());
 Assert.assertEquals(officeMath.getParentNode(), officeMath.getParentParagraph());

 // Change the location and display type of the OfficeMath node.
 officeMath.setDisplayType(OfficeMathDisplayType.DISPLAY);
 officeMath.setJustification(OfficeMathJustification.LEFT);

 doc.save(getArtifactsDir() + "Shape.OfficeMath.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [DISPLAY](#DISPLAY) | The Office Math is displayed on its own line. |
| [INLINE](#INLINE) | The Office Math is displayed inline with the text. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String officeMathDisplayTypeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int officeMathDisplayType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int officeMathDisplayType)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### DISPLAY {#DISPLAY}
```
public static int DISPLAY
```


The Office Math is displayed on its own line.

### INLINE {#INLINE}
```
public static int INLINE
```


The Office Math is displayed inline with the text.

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
### fromName(String officeMathDisplayTypeName) {#fromName-java.lang.String}
```
public static int fromName(String officeMathDisplayTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| officeMathDisplayTypeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int officeMathDisplayType) {#getName-int}
```
public static String getName(int officeMathDisplayType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| officeMathDisplayType | int |  |

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
### toString(int officeMathDisplayType) {#toString-int}
```
public static String toString(int officeMathDisplayType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| officeMathDisplayType | int |  |

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

