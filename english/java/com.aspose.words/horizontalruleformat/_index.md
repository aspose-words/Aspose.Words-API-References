---
title: HorizontalRuleFormat
linktitle: HorizontalRuleFormat
second_title: Aspose.Words for Java
description: Represents horizontal rule formatting in Java.
type: docs
weight: 355
url: /java/com.aspose.words/horizontalruleformat/
---

**Inheritance:**
java.lang.Object
```
public class HorizontalRuleFormat
```

Represents horizontal rule formatting.

To learn more, visit the [ Working with Shapes ][Working with Shapes] documentation article.

 **Examples:** 

Shows how to insert a horizontal rule shape, and customize its formatting.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```


[Working with Shapes]: https://docs.aspose.com/words/java/working-with-shapes/
## Methods

| Method | Description |
| --- | --- |
| [getAlignment()](#getAlignment) | Gets the alignment of the horizontal rule. |
| [getColor()](#getColor) | Gets the brush color that fills the horizontal rule. |
| [getHeight()](#getHeight) | Gets the height of the horizontal rule. |
| [getNoShade()](#getNoShade) | Indicates the presence of 3D shading for the horizontal rule. |
| [getWidthPercent()](#getWidthPercent) | Gets the length of the specified horizontal rule expressed as a percentage of the window width. |
| [setAlignment(int value)](#setAlignment-int) | Sets the alignment of the horizontal rule. |
| [setColor(Color value)](#setColor-java.awt.Color) | Sets the brush color that fills the horizontal rule. |
| [setHeight(double value)](#setHeight-double) | Sets the height of the horizontal rule. |
| [setNoShade(boolean value)](#setNoShade-boolean) | Indicates the presence of 3D shading for the horizontal rule. |
| [setWidthPercent(double value)](#setWidthPercent-double) | Sets the length of the specified horizontal rule expressed as a percentage of the window width. |
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Gets the alignment of the horizontal rule.

 **Remarks:** 

The default value is [HorizontalRuleAlignment.LEFT](../../com.aspose.words/horizontalrulealignment/\#LEFT).

 **Examples:** 

Shows how to insert a horizontal rule shape, and customize its formatting.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
int - The alignment of the horizontal rule. The returned value is one of [HorizontalRuleAlignment](../../com.aspose.words/horizontalrulealignment/) constants.
### getColor() {#getColor}
```
public Color getColor()
```


Gets the brush color that fills the horizontal rule.

 **Remarks:** 

This is a shortcut to the [Fill.getColor()](../../com.aspose.words/fill/\#getColor) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color) property.

The default value is java.awt.Color\#getGray().getGray().

 **Examples:** 

Shows how to insert a horizontal rule shape, and customize its formatting.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
java.awt.Color - The brush color that fills the horizontal rule.
### getHeight() {#getHeight}
```
public double getHeight()
```


Gets the height of the horizontal rule.

**Returns:**
double - The height of the horizontal rule.
### getNoShade() {#getNoShade}
```
public boolean getNoShade()
```


Indicates the presence of 3D shading for the horizontal rule. If  true , then the horizontal rule is without 3D shading and solid color is used.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows how to insert a horizontal rule shape, and customize its formatting.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getWidthPercent() {#getWidthPercent}
```
public double getWidthPercent()
```


Gets the length of the specified horizontal rule expressed as a percentage of the window width.

**Returns:**
double - The length of the specified horizontal rule expressed as a percentage of the window width.
### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Sets the alignment of the horizontal rule.

 **Remarks:** 

The default value is [HorizontalRuleAlignment.LEFT](../../com.aspose.words/horizontalrulealignment/\#LEFT).

 **Examples:** 

Shows how to insert a horizontal rule shape, and customize its formatting.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The alignment of the horizontal rule. The value must be one of [HorizontalRuleAlignment](../../com.aspose.words/horizontalrulealignment/) constants. |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Sets the brush color that fills the horizontal rule.

 **Remarks:** 

This is a shortcut to the [Fill.getColor()](../../com.aspose.words/fill/\#getColor) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color) property.

The default value is java.awt.Color\#getGray().getGray().

 **Examples:** 

Shows how to insert a horizontal rule shape, and customize its formatting.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The brush color that fills the horizontal rule. |

### setHeight(double value) {#setHeight-double}
```
public void setHeight(double value)
```


Sets the height of the horizontal rule.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The height of the horizontal rule. |

### setNoShade(boolean value) {#setNoShade-boolean}
```
public void setNoShade(boolean value)
```


Indicates the presence of 3D shading for the horizontal rule. If  true , then the horizontal rule is without 3D shading and solid color is used.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows how to insert a horizontal rule shape, and customize its formatting.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setWidthPercent(double value) {#setWidthPercent-double}
```
public void setWidthPercent(double value)
```


Sets the length of the specified horizontal rule expressed as a percentage of the window width.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The length of the specified horizontal rule expressed as a percentage of the window width. |

