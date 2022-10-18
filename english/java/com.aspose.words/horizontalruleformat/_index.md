---
title: HorizontalRuleFormat
second_title: Aspose.Words for Java API Reference
description: Represents horizontal rule formatting.
type: docs
weight: 322
url: /java/com.aspose.words/horizontalruleformat/
---

**Inheritance:**
java.lang.Object
```
public class HorizontalRuleFormat
```

Represents horizontal rule formatting.

To learn more, visit the **Working with Shapes** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getWidthPercent()](#getWidthPercent--) | Gets the length of the specified horizontal rule expressed as a percentage of the window width. |
| [setWidthPercent(double value)](#setWidthPercent-double-) | Sets the length of the specified horizontal rule expressed as a percentage of the window width. |
| [getHeight()](#getHeight--) | Gets the height of the horizontal rule. |
| [setHeight(double value)](#setHeight-double-) | Sets the height of the horizontal rule. |
| [getNoShade()](#getNoShade--) | Indicates the presence of 3D shading for the horizontal rule. |
| [setNoShade(boolean value)](#setNoShade-boolean-) | Indicates the presence of 3D shading for the horizontal rule. |
| [getColor()](#getColor--) | Gets the brush color that fills the horizontal rule. |
| [setColor(Color value)](#setColor-java.awt.Color-) | Sets the brush color that fills the horizontal rule. |
| [getAlignment()](#getAlignment--) | Gets the alignment of the horizontal rule. |
| [setAlignment(int value)](#setAlignment-int-) | Sets the alignment of the horizontal rule. |
### getWidthPercent() {#getWidthPercent--}
```
public double getWidthPercent()
```


Gets the length of the specified horizontal rule expressed as a percentage of the window width.

Valid values \\u200b\\u200brange from 1 to 100 inclusive.

The default value is 100.

**Returns:**
double - The length of the specified horizontal rule expressed as a percentage of the window width.
### setWidthPercent(double value) {#setWidthPercent-double-}
```
public void setWidthPercent(double value)
```


Sets the length of the specified horizontal rule expressed as a percentage of the window width.

Valid values \\u200b\\u200brange from 1 to 100 inclusive.

The default value is 100.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The length of the specified horizontal rule expressed as a percentage of the window width. |

### getHeight() {#getHeight--}
```
public double getHeight()
```


Gets the height of the horizontal rule.

This is a shortcut to the [ShapeBase.getHeight()](../../com.aspose.words/shapebase\#getHeight--) / [ShapeBase.setHeight(double)](../../com.aspose.words/shapebase\#setHeight-double-) property.

Valid values \\u200b\\u200brange from 0 to 1584 inclusive.

The default value is 1.5.

**Returns:**
double - The height of the horizontal rule.
### setHeight(double value) {#setHeight-double-}
```
public void setHeight(double value)
```


Sets the height of the horizontal rule.

This is a shortcut to the [ShapeBase.getHeight()](../../com.aspose.words/shapebase\#getHeight--) / [ShapeBase.setHeight(double)](../../com.aspose.words/shapebase\#setHeight-double-) property.

Valid values \\u200b\\u200brange from 0 to 1584 inclusive.

The default value is 1.5.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The height of the horizontal rule. |

### getNoShade() {#getNoShade--}
```
public boolean getNoShade()
```


Indicates the presence of 3D shading for the horizontal rule. If true, then the horizontal rule is without 3D shading and solid color is used.

The default value is false.

**Returns:**
boolean - The corresponding  boolean  value.
### setNoShade(boolean value) {#setNoShade-boolean-}
```
public void setNoShade(boolean value)
```


Indicates the presence of 3D shading for the horizontal rule. If true, then the horizontal rule is without 3D shading and solid color is used.

The default value is false.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getColor() {#getColor--}
```
public Color getColor()
```


Gets the brush color that fills the horizontal rule.

This is a shortcut to the [Fill.getColor()](../../com.aspose.words/fill\#getColor--) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill\#setColor-java.awt.Color-) property.

The default value is .

**Returns:**
java.awt.Color - The brush color that fills the horizontal rule.
### setColor(Color value) {#setColor-java.awt.Color-}
```
public void setColor(Color value)
```


Sets the brush color that fills the horizontal rule.

This is a shortcut to the [Fill.getColor()](../../com.aspose.words/fill\#getColor--) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill\#setColor-java.awt.Color-) property.

The default value is .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The brush color that fills the horizontal rule. |

### getAlignment() {#getAlignment--}
```
public int getAlignment()
```


Gets the alignment of the horizontal rule.

The default value is [HorizontalRuleAlignment.LEFT](../../com.aspose.words/horizontalrulealignment\#LEFT).

**Returns:**
int - The alignment of the horizontal rule. The returned value is one of [HorizontalRuleAlignment](../../com.aspose.words/horizontalrulealignment) constants.
### setAlignment(int value) {#setAlignment-int-}
```
public void setAlignment(int value)
```


Sets the alignment of the horizontal rule.

The default value is [HorizontalRuleAlignment.LEFT](../../com.aspose.words/horizontalrulealignment\#LEFT).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The alignment of the horizontal rule. The value must be one of [HorizontalRuleAlignment](../../com.aspose.words/horizontalrulealignment) constants. |

