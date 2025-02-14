---
title: ShadowFormat
linktitle: ShadowFormat
second_title: Aspose.Words for Java
description: Represents shadow formatting for an object in Java.
type: docs
weight: 590
url: /java/com.aspose.words/shadowformat/
---

**Inheritance:**
java.lang.Object
```
public class ShadowFormat
```

Represents shadow formatting for an object.

To learn more, visit the [ Working with Graphic Elements ][Working with Graphic Elements] documentation article.

 **Examples:** 

Shows how to get shadow color.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```


[Working with Graphic Elements]: https://docs.aspose.com/words/java/working-with-graphic-elements/
## Methods

| Method | Description |
| --- | --- |
| [clear()](#clear) | Clears shadow format. |
| [getColor()](#getColor) | Gets a java.awt.Color object that represents the color for the shadow. |
| [getType()](#getType) | Gets the specified [ShadowType](../../com.aspose.words/shadowtype/) for ShadowFormat. |
| [getVisible()](#getVisible) | Returns  true  if the formatting applied to this instance is visible. |
| [setType(int value)](#setType-int) | Sets the specified [ShadowType](../../com.aspose.words/shadowtype/) for ShadowFormat. |
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

### getColor() {#getColor}
```
public Color getColor()
```


Gets a java.awt.Color object that represents the color for the shadow. The default value is java.awt.Color\#getBlack().getBlack().

 **Examples:** 

Shows how to get shadow color.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

**Returns:**
java.awt.Color - A java.awt.Color object that represents the color for the shadow.
### getType() {#getType}
```
public int getType()
```


Gets the specified [ShadowType](../../com.aspose.words/shadowtype/) for ShadowFormat.

 **Examples:** 

Shows how to get shadow color.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

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
### setType(int value) {#setType-int}
```
public void setType(int value)
```


Sets the specified [ShadowType](../../com.aspose.words/shadowtype/) for ShadowFormat.

 **Examples:** 

Shows how to get shadow color.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The specified [ShadowType](../../com.aspose.words/shadowtype/) for ShadowFormat. The value must be one of [ShadowType](../../com.aspose.words/shadowtype/) constants. |

