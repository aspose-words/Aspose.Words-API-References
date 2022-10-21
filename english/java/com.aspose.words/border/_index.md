---
title: Border
second_title: Aspose.Words for Java API Reference
description: Represents a border of an object.
type: docs
weight: 36
url: /java/com.aspose.words/border/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Border extends InternableComplexAttr implements Cloneable
```

Represents a border of an object.

To learn more, visit the **Programming with Documents** documentation article.

Borders can be applied to various document elements including paragraph, run of text inside a paragraph or a table cell.
## Methods

| Method | Description |
| --- | --- |
| [clearFormatting()](#clearFormatting--) | Resets border properties to default values. |
| [getLineStyle()](#getLineStyle--) | Gets the border style. |
| [setLineStyle(int value)](#setLineStyle-int-) | Sets the border style. |
| [getLineWidth()](#getLineWidth--) | Gets the border width in points. |
| [setLineWidth(double value)](#setLineWidth-double-) | Sets the border width in points. |
| [isVisible()](#isVisible--) | Returns true if the LineStyle is not LineStyle.None. |
| [getColor()](#getColor--) | Gets the border color. |
| [setColor(Color value)](#setColor-java.awt.Color-) | Sets the border color. |
| [getDistanceFromText()](#getDistanceFromText--) | Gets distance of the border from text or from the page edge in points. |
| [setDistanceFromText(double value)](#setDistanceFromText-double-) | Sets distance of the border from text or from the page edge in points. |
| [getShadow()](#getShadow--) | Gets a value indicating whether the border has a shadow. |
| [setShadow(boolean value)](#setShadow-boolean-) | Sets a value indicating whether the border has a shadow. |
| [equals(Border rhs)](#equals-com.aspose.words.Border-) | Determines whether the specified border is equal in value to the current border. |
| [equals(Object obj)](#equals-java.lang.Object-) | Determines whether the specified object is equal in value to the current object. |
| [hashCode()](#hashCode--) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr--) |  |
### clearFormatting() {#clearFormatting--}
```
public void clearFormatting()
```


Resets border properties to default values. When border properties are reset to default values, the border is invisible.

### getLineStyle() {#getLineStyle--}
```
public int getLineStyle()
```


Gets the border style.

If you set line style to none, then line width is automatically changed to zero.

**Returns:**
int - The border style. The returned value is one of [LineStyle](../../com.aspose.words/linestyle) constants.
### setLineStyle(int value) {#setLineStyle-int-}
```
public void setLineStyle(int value)
```


Sets the border style.

If you set line style to none, then line width is automatically changed to zero.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The border style. The value must be one of [LineStyle](../../com.aspose.words/linestyle) constants. |

### getLineWidth() {#getLineWidth--}
```
public double getLineWidth()
```


Gets the border width in points.

If you set line width greater than zero when line style is none, the line style is automatically changed to single line.

**Returns:**
double - The border width in points.
### setLineWidth(double value) {#setLineWidth-double-}
```
public void setLineWidth(double value)
```


Sets the border width in points.

If you set line width greater than zero when line style is none, the line style is automatically changed to single line.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The border width in points. |

### isVisible() {#isVisible--}
```
public boolean isVisible()
```


Returns true if the LineStyle is not LineStyle.None.

**Returns:**
boolean - True if the LineStyle is not LineStyle.None.
### getColor() {#getColor--}
```
public Color getColor()
```


Gets the border color.

**Returns:**
java.awt.Color - The border color.
### setColor(Color value) {#setColor-java.awt.Color-}
```
public void setColor(Color value)
```


Sets the border color.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The border color. |

### getDistanceFromText() {#getDistanceFromText--}
```
public double getDistanceFromText()
```


Gets distance of the border from text or from the page edge in points. Has no effect and will be automatically reset to zero for borders of table cells.

**Returns:**
double - Distance of the border from text or from the page edge in points.
### setDistanceFromText(double value) {#setDistanceFromText-double-}
```
public void setDistanceFromText(double value)
```


Sets distance of the border from text or from the page edge in points. Has no effect and will be automatically reset to zero for borders of table cells.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | Distance of the border from text or from the page edge in points. |

### getShadow() {#getShadow--}
```
public boolean getShadow()
```


Gets a value indicating whether the border has a shadow.

In Microsoft Word, for a border to have a shadow, the borders on all four sides (left, top, right and bottom) should be of the same type, width, color and all should have the Shadow property set to true.

**Returns:**
boolean - A value indicating whether the border has a shadow.
### setShadow(boolean value) {#setShadow-boolean-}
```
public void setShadow(boolean value)
```


Sets a value indicating whether the border has a shadow.

In Microsoft Word, for a border to have a shadow, the borders on all four sides (left, top, right and bottom) should be of the same type, width, color and all should have the Shadow property set to true.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether the border has a shadow. |

### equals(Border rhs) {#equals-com.aspose.words.Border-}
```
public boolean equals(Border rhs)
```


Determines whether the specified border is equal in value to the current border.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rhs | [Border](../../com.aspose.words/border) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object-}
```
public boolean equals(Object obj)
```


Determines whether the specified object is equal in value to the current object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### hashCode() {#hashCode--}
```
public int hashCode()
```




**Returns:**
int
### isInheritedComplexAttr() {#isInheritedComplexAttr--}
```
public boolean isInheritedComplexAttr()
```




**Returns:**
boolean
