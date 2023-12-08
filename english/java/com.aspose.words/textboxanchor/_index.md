---
title: TextBoxAnchor
linktitle: TextBoxAnchor
second_title: Aspose.Words for Java
description: Specifies values used for shape text vertical alignment in Java.
type: docs
weight: 586
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
| [fromName(String textBoxAnchorName)](#fromName-java.lang.String) |  |
| [getName(int textBoxAnchor)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textBoxAnchor)](#toString-int) |  |
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
