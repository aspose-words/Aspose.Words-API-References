---
title: TextBoxAnchor
linktitle: TextBoxAnchor
second_title: Aspose.Words for Java API Reference
description: Specifies values used for shape text vertical alignment in Java.
type: docs
weight: 568
url: /java/com.aspose.words/textboxanchor/
---

**Inheritance:**
java.lang.Object
```
public class TextBoxAnchor
```

Specifies values used for shape text vertical alignment.

 **Examples:** 

Shows how to vertically align the text contents of a text box.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.TEXT_BOX, 200.0, 200.0);

 // Set the "VerticalAnchor" property to "TextBoxAnchor.Top" to
 // align the text in this text box with the top side of the shape.
 // Set the "VerticalAnchor" property to "TextBoxAnchor.Middle" to
 // align the text in this text box to the center of the shape.
 // Set the "VerticalAnchor" property to "TextBoxAnchor.Bottom" to
 // align the text in this text box to the bottom of the shape.
 shape.getTextBox().setVerticalAnchor(verticalAnchor);

 builder.moveTo(shape.getFirstParagraph());
 builder.write("Hello world!");

 // The vertical aligning of text inside text boxes is available from Microsoft Word 2007 onwards.
 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2007);
 doc.save(getArtifactsDir() + "Shape.VerticalAnchor.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [BOTTOM](#BOTTOM) | Text is aligned to the bottom of the textbox. |
| [BOTTOM_BASELINE](#BOTTOM-BASELINE) | Text is aligned to the bottom baseline of the textbox. |
| [BOTTOM_CENTERED](#BOTTOM-CENTERED) | Text is aligned to the bottom centered of the textbox. |
| [BOTTOM_CENTERED_BASELINE](#BOTTOM-CENTERED-BASELINE) | Text is aligned to the bottom centered baseline of the textbox. |
| [MIDDLE](#MIDDLE) | Text is aligned to the middle of the textbox. |
| [MIDDLE_CENTERED](#MIDDLE-CENTERED) | Text is aligned to the middle centered of the textbox. |
| [TOP](#TOP) | Text is aligned to the top of the textbox. |
| [TOP_BASELINE](#TOP-BASELINE) | Text is aligned to the top baseline of the textbox. |
| [TOP_CENTERED](#TOP-CENTERED) | Text is aligned to the top centered of the textbox. |
| [TOP_CENTERED_BASELINE](#TOP-CENTERED-BASELINE) | Text is aligned to the top centered baseline of the textbox. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String textBoxAnchorName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int textBoxAnchor)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int textBoxAnchor)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Text is aligned to the bottom of the textbox.

### BOTTOM_BASELINE {#BOTTOM-BASELINE}
```
public static int BOTTOM_BASELINE
```


Text is aligned to the bottom baseline of the textbox.

### BOTTOM_CENTERED {#BOTTOM-CENTERED}
```
public static int BOTTOM_CENTERED
```


Text is aligned to the bottom centered of the textbox.

### BOTTOM_CENTERED_BASELINE {#BOTTOM-CENTERED-BASELINE}
```
public static int BOTTOM_CENTERED_BASELINE
```


Text is aligned to the bottom centered baseline of the textbox.

### MIDDLE {#MIDDLE}
```
public static int MIDDLE
```


Text is aligned to the middle of the textbox.

### MIDDLE_CENTERED {#MIDDLE-CENTERED}
```
public static int MIDDLE_CENTERED
```


Text is aligned to the middle centered of the textbox.

### TOP {#TOP}
```
public static int TOP
```


Text is aligned to the top of the textbox.

### TOP_BASELINE {#TOP-BASELINE}
```
public static int TOP_BASELINE
```


Text is aligned to the top baseline of the textbox.

### TOP_CENTERED {#TOP-CENTERED}
```
public static int TOP_CENTERED
```


Text is aligned to the top centered of the textbox.

### TOP_CENTERED_BASELINE {#TOP-CENTERED-BASELINE}
```
public static int TOP_CENTERED_BASELINE
```


Text is aligned to the top centered baseline of the textbox.

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
### fromName(String textBoxAnchorName) {#fromName-java.lang.String}
```
public static int fromName(String textBoxAnchorName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| textBoxAnchorName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int textBoxAnchor) {#getName-int}
```
public static String getName(int textBoxAnchor)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| textBoxAnchor | int |  |

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
### toString(int textBoxAnchor) {#toString-int}
```
public static String toString(int textBoxAnchor)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| textBoxAnchor | int |  |

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

