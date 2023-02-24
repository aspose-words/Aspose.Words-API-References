---
title: Border
linktitle: Border
second_title: Aspose.Words for Java API Reference
description: Represents a border of an object in Java.
type: docs
weight: 36
url: /java/com.aspose.words/border/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Border extends InternableComplexAttr implements Cloneable
```

Represents a border of an object.

To learn more, visit the [ Programming with Documents ][Programming with Documents] documentation article.

Borders can be applied to various document elements including paragraph, run of text inside a paragraph or a table cell.


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Methods

| Method | Description |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Resets border properties to default values. |
| [equals(Border rhs)](#equals-com.aspose.words.Border) | Determines whether the specified border is equal in value to the current border. |
| [equals(Object obj)](#equals-java.lang.Object) | Determines whether the specified object is equal in value to the current object. |
| [getClass()](#getClass) |  |
| [getColor()](#getColor) | Gets the border color. |
| [getDistanceFromText()](#getDistanceFromText) | Gets distance of the border from text or from the page edge in points. |
| [getLineStyle()](#getLineStyle) | Gets the border style. |
| [getLineWidth()](#getLineWidth) | Gets the border width in points. |
| [getShadow()](#getShadow) | Gets a value indicating whether the border has a shadow. |
| [getThemeColor()](#getThemeColor) | Gets the theme color in the applied color scheme that is associated with this Border object. |
| [getTintAndShade()](#getTintAndShade) | Gets a double value that lightens or darkens a color. |
| [hashCode()](#hashCode) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [isVisible()](#isVisible) | Returns  true  if the [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) is not [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE). |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setColor(Color value)](#setColor-java.awt.Color) | Sets the border color. |
| [setDistanceFromText(double value)](#setDistanceFromText-double) | Sets distance of the border from text or from the page edge in points. |
| [setLineStyle(int value)](#setLineStyle-int) | Sets the border style. |
| [setLineWidth(double value)](#setLineWidth-double) | Sets the border width in points. |
| [setShadow(boolean value)](#setShadow-boolean) | Sets a value indicating whether the border has a shadow. |
| [setThemeColor(int value)](#setThemeColor-int) | Sets the theme color in the applied color scheme that is associated with this Border object. |
| [setTintAndShade(double value)](#setTintAndShade-double) | Sets a double value that lightens or darkens a color. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Resets border properties to default values. When border properties are reset to default values, the border is invisible.

### equals(Border rhs) {#equals-com.aspose.words.Border}
```
public boolean equals(Border rhs)
```


Determines whether the specified border is equal in value to the current border.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rhs | [Border](../../com.aspose.words/border/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getColor() {#getColor}
```
public Color getColor()
```


Gets the border color.

**Returns:**
java.awt.Color - The border color.
### getDistanceFromText() {#getDistanceFromText}
```
public double getDistanceFromText()
```


Gets distance of the border from text or from the page edge in points. Has no effect and will be automatically reset to zero for borders of table cells.

**Returns:**
double - Distance of the border from text or from the page edge in points.
### getLineStyle() {#getLineStyle}
```
public int getLineStyle()
```


Gets the border style.

If you set line style to none, then line width is automatically changed to zero.

**Returns:**
int - The border style. The returned value is one of [LineStyle](../../com.aspose.words/linestyle/) constants.
### getLineWidth() {#getLineWidth}
```
public double getLineWidth()
```


Gets the border width in points.

If you set line width greater than zero when line style is none, the line style is automatically changed to single line.

**Returns:**
double - The border width in points.
### getShadow() {#getShadow}
```
public boolean getShadow()
```


Gets a value indicating whether the border has a shadow.

In Microsoft Word, for a border to have a shadow, the borders on all four sides (left, top, right and bottom) should be of the same type, width, color and all should have the Shadow property set to  true .

**Returns:**
boolean - A value indicating whether the border has a shadow.
### getThemeColor() {#getThemeColor}
```
public int getThemeColor()
```


Gets the theme color in the applied color scheme that is associated with this Border object.

**Returns:**
int - The theme color in the applied color scheme that is associated with this Border object. The returned value is one of [ThemeColor](../../com.aspose.words/themecolor/) constants.
### getTintAndShade() {#getTintAndShade}
```
public double getTintAndShade()
```


Gets a double value that lightens or darkens a color.

The allowed values are in the range from -1 (the darkest) to 1 (the lightest) for this property. Zero (0) is neutral. Attempting to set this property to a value less than -1 or more than 1 results in java.lang.IllegalArgumentException.

Setting this property for Border object with non-theme colors results in java.lang.IllegalStateException.

**Returns:**
double - A double value that lightens or darkens a color.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### isInheritedComplexAttr() {#isInheritedComplexAttr}
```
public boolean isInheritedComplexAttr()
```




**Returns:**
boolean
### isVisible() {#isVisible}
```
public boolean isVisible()
```


Returns  true  if the [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) is not [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE).

**Returns:**
boolean - \{ true  if the [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) is not [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE).
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Sets the border color.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The border color. |

### setDistanceFromText(double value) {#setDistanceFromText-double}
```
public void setDistanceFromText(double value)
```


Sets distance of the border from text or from the page edge in points. Has no effect and will be automatically reset to zero for borders of table cells.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | Distance of the border from text or from the page edge in points. |

### setLineStyle(int value) {#setLineStyle-int}
```
public void setLineStyle(int value)
```


Sets the border style.

If you set line style to none, then line width is automatically changed to zero.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The border style. The value must be one of [LineStyle](../../com.aspose.words/linestyle/) constants. |

### setLineWidth(double value) {#setLineWidth-double}
```
public void setLineWidth(double value)
```


Sets the border width in points.

If you set line width greater than zero when line style is none, the line style is automatically changed to single line.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The border width in points. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


Sets a value indicating whether the border has a shadow.

In Microsoft Word, for a border to have a shadow, the borders on all four sides (left, top, right and bottom) should be of the same type, width, color and all should have the Shadow property set to  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether the border has a shadow. |

### setThemeColor(int value) {#setThemeColor-int}
```
public void setThemeColor(int value)
```


Sets the theme color in the applied color scheme that is associated with this Border object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The theme color in the applied color scheme that is associated with this Border object. The value must be one of [ThemeColor](../../com.aspose.words/themecolor/) constants. |

### setTintAndShade(double value) {#setTintAndShade-double}
```
public void setTintAndShade(double value)
```


Sets a double value that lightens or darkens a color.

The allowed values are in the range from -1 (the darkest) to 1 (the lightest) for this property. Zero (0) is neutral. Attempting to set this property to a value less than -1 or more than 1 results in java.lang.IllegalArgumentException.

Setting this property for Border object with non-theme colors results in java.lang.IllegalStateException.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | A double value that lightens or darkens a color. |

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

