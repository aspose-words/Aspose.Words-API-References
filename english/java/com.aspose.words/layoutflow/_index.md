---
title: LayoutFlow
linktitle: LayoutFlow
second_title: Aspose.Words for Java
description: Determines the flow of the text layout in a textbox in Java.
type: docs
weight: 403
url: /java/com.aspose.words/layoutflow/
---

**Inheritance:**
java.lang.Object
```
public class LayoutFlow
```

Determines the flow of the text layout in a textbox.

 **Examples:** 

Shows how to add text to a text box, and change its orientation.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape textbox = new Shape(doc, ShapeType.TEXT_BOX);
 textbox.setWidth(100.0);
 textbox.setHeight(100.0);
 textbox.getTextBox().setLayoutFlow(LayoutFlow.BOTTOM_TO_TOP);

 textbox.appendChild(new Paragraph(doc));
 builder.insertNode(textbox);

 builder.moveTo(textbox.getFirstParagraph());
 builder.write("This text is flipped 90 degrees to the left.");

 doc.save(getArtifactsDir() + "Drawing.TextBox.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [BOTTOM_TO_TOP](#BOTTOM-TO-TOP) | Text is displayed vertically. |
| [HORIZONTAL](#HORIZONTAL) | Text is displayed horizontally. |
| [HORIZONTAL_IDEOGRAPHIC](#HORIZONTAL-IDEOGRAPHIC) | Ideographic text is displayed horizontally. |
| [TOP_TO_BOTTOM](#TOP-TO-BOTTOM) | Text is displayed vertically. |
| [TOP_TO_BOTTOM_IDEOGRAPHIC](#TOP-TO-BOTTOM-IDEOGRAPHIC) | Ideographic text is displayed vertically. |
| [VERTICAL](#VERTICAL) | Text is displayed vertically. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String layoutFlowName)](#fromName-java.lang.String) |  |
| [getName(int layoutFlow)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int layoutFlow)](#toString-int) |  |
### BOTTOM_TO_TOP {#BOTTOM-TO-TOP}
```
public static int BOTTOM_TO_TOP
```


Text is displayed vertically.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Text is displayed horizontally.

### HORIZONTAL_IDEOGRAPHIC {#HORIZONTAL-IDEOGRAPHIC}
```
public static int HORIZONTAL_IDEOGRAPHIC
```


Ideographic text is displayed horizontally.

### TOP_TO_BOTTOM {#TOP-TO-BOTTOM}
```
public static int TOP_TO_BOTTOM
```


Text is displayed vertically.

### TOP_TO_BOTTOM_IDEOGRAPHIC {#TOP-TO-BOTTOM-IDEOGRAPHIC}
```
public static int TOP_TO_BOTTOM_IDEOGRAPHIC
```


Ideographic text is displayed vertically.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Text is displayed vertically.

### length {#length}
```
public static int length
```


### fromName(String layoutFlowName) {#fromName-java.lang.String}
```
public static int fromName(String layoutFlowName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| layoutFlowName | java.lang.String |  |

**Returns:**
int
### getName(int layoutFlow) {#getName-int}
```
public static String getName(int layoutFlow)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| layoutFlow | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int layoutFlow) {#toString-int}
```
public static String toString(int layoutFlow)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| layoutFlow | int |  |

**Returns:**
java.lang.String
