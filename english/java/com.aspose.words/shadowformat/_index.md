---
title: ShadowFormat
linktitle: ShadowFormat
second_title: Aspose.Words for Java
description: Represents shadow formatting for an object in Java.
type: docs
weight: 534
url: /java/com.aspose.words/shadowformat/
---

**Inheritance:**
java.lang.Object
```
public class ShadowFormat
```

Represents shadow formatting for an object.

To learn more, visit the [ Working with Graphic Elements ][Working with Graphic Elements] documentation article.


[Working with Graphic Elements]: https://docs.aspose.com/words/java/working-with-graphic-elements/
## Methods

| Method | Description |
| --- | --- |
| [clear()](#clear) | Clears shadow format. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getType()](#getType) | Gets the specified [ShadowType](../../com.aspose.words/shadowtype/) for ShadowFormat. |
| [getVisible()](#getVisible) | Returns  true  if the formatting applied to this instance is visible. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setType(int value)](#setType-int) | Sets the specified [ShadowType](../../com.aspose.words/shadowtype/) for ShadowFormat. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### clear() {#clear}
```
public void clear()
```


Clears shadow format.

 **Examples:** 

Shows how to work with a shadow formatting for the shape.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape)doc.getChildNodes(NodeType.SHAPE, true).get(0);

 if (shape.getShadowFormat().getVisible() && shape.getShadowFormat().getType() == ShadowType.SHADOW_2)
     shape.getShadowFormat().setType(ShadowType.SHADOW_7);

 if (shape.getShadowFormat().getType() == ShadowType.SHADOW_MIXED)
     shape.getShadowFormat().clear();
 
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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getType() {#getType}
```
public int getType()
```


Gets the specified [ShadowType](../../com.aspose.words/shadowtype/) for ShadowFormat.

**Returns:**
int - The specified [ShadowType](../../com.aspose.words/shadowtype/) for ShadowFormat. The returned value is one of [ShadowType](../../com.aspose.words/shadowtype/) constants.
### getVisible() {#getVisible}
```
public boolean getVisible()
```


Returns  true  if the formatting applied to this instance is visible.

 **Remarks:** 

Unlike [clear()](../../com.aspose.words/shadowformat/\#clear), assigning  false  to Visible does not clear the formatting, it only hides the shape effect.

 **Examples:** 

Shows how to work with a shadow formatting for the shape.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape)doc.getChildNodes(NodeType.SHAPE, true).get(0);

 if (shape.getShadowFormat().getVisible() && shape.getShadowFormat().getType() == ShadowType.SHADOW_2)
     shape.getShadowFormat().setType(ShadowType.SHADOW_7);

 if (shape.getShadowFormat().getType() == ShadowType.SHADOW_MIXED)
     shape.getShadowFormat().clear();
 
```

**Returns:**
boolean -  true  if the formatting applied to this instance is visible.
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




### setType(int value) {#setType-int}
```
public void setType(int value)
```


Sets the specified [ShadowType](../../com.aspose.words/shadowtype/) for ShadowFormat.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The specified [ShadowType](../../com.aspose.words/shadowtype/) for ShadowFormat. The value must be one of [ShadowType](../../com.aspose.words/shadowtype/) constants. |

### toString() {#toString}
```
public String toString()
```




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

