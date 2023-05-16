---
title: OfficeMathJustification
linktitle: OfficeMathJustification
second_title: Aspose.Words for Java
description: Specifies the justification of the equation in Java.
type: docs
weight: 439
url: /java/com.aspose.words/officemathjustification/
---

**Inheritance:**
java.lang.Object
```
public class OfficeMathJustification
```

Specifies the justification of the equation.

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
| [CENTER](#CENTER) | Centers each instance of mathematical text individually with respect to margins. |
| [CENTER_GROUP](#CENTER-GROUP) | Justifies instances of mathematical text to the left with respect to each other, and centers the group of mathematical text (the Math Paragraph) with respect to the page. |
| [DEFAULT](#DEFAULT) | Default value [CENTER\_GROUP](../../com.aspose.words/officemathjustification/\#CENTER-GROUP). |
| [INLINE](#INLINE) | Inline position of Math. |
| [LEFT](#LEFT) | Left justification of Math Paragraph. |
| [RIGHT](#RIGHT) | Right Justification of Math Paragraph. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String officeMathJustificationName)](#fromName-java.lang.String) |  |
| [getName(int officeMathJustification)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int officeMathJustification)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Centers each instance of mathematical text individually with respect to margins.

### CENTER_GROUP {#CENTER-GROUP}
```
public static int CENTER_GROUP
```


Justifies instances of mathematical text to the left with respect to each other, and centers the group of mathematical text (the Math Paragraph) with respect to the page.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Default value [CENTER\_GROUP](../../com.aspose.words/officemathjustification/\#CENTER-GROUP).

### INLINE {#INLINE}
```
public static int INLINE
```


Inline position of Math.

### LEFT {#LEFT}
```
public static int LEFT
```


Left justification of Math Paragraph.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Right Justification of Math Paragraph.

### length {#length}
```
public static int length
```


### fromName(String officeMathJustificationName) {#fromName-java.lang.String}
```
public static int fromName(String officeMathJustificationName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| officeMathJustificationName | java.lang.String |  |

**Returns:**
int
### getName(int officeMathJustification) {#getName-int}
```
public static String getName(int officeMathJustification)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| officeMathJustification | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int officeMathJustification) {#toString-int}
```
public static String toString(int officeMathJustification)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| officeMathJustification | int |  |

**Returns:**
java.lang.String
