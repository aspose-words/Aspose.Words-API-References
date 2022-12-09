---
title: Stroke
second_title: Aspose.Words for Java API Reference
description: Defines a stroke for a shape.
type: docs
weight: 534
url: /java/com.aspose.words/stroke/
---

**Inheritance:**
java.lang.Object
```
public class Stroke
```

Defines a stroke for a shape.

To learn more, visit the [ Working with Shapes ][Working with Shapes] documentation article.

Use the [Shape.getStroke()](../../com.aspose.words/shape\#getStroke) property to access stroke properties of a shape. You do not create instances of the [Stroke](../../com.aspose.words/stroke) class directly.


[Working with Shapes]: https://docs.aspose.com/words/java/working-with-shapes/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getBackColor()](#getBackColor) | Gets the background color of the stroke. |
| [getClass()](#getClass) |  |
| [getColor()](#getColor) | Defines the color of a stroke. |
| [getColor2()](#getColor2) | Defines a second color for a stroke. |
| [getDashStyle()](#getDashStyle) | Specifies the dot and dash pattern for a stroke. |
| [getEndArrowLength()](#getEndArrowLength) | Defines the arrowhead length for the end of a stroke. |
| [getEndArrowType()](#getEndArrowType) | Defines the arrowhead for the end of a stroke. |
| [getEndArrowWidth()](#getEndArrowWidth) | Defines the arrowhead width for the end of a stroke. |
| [getEndCap()](#getEndCap) | Defines the cap style for the end of a stroke. |
| [getForeColor()](#getForeColor) | Gets the foreground color of the stroke. |
| [getImageBytes()](#getImageBytes) | Defines the image for a stroke image or pattern fill. |
| [getJoinStyle()](#getJoinStyle) | Defines the join style of a polyline. |
| [getLineStyle()](#getLineStyle) | Defines the line style of the stroke. |
| [getOn()](#getOn) | Defines whether the path will be stroked. |
| [getOpacity()](#getOpacity) | Defines the amount of transparency of a stroke. |
| [getStartArrowLength()](#getStartArrowLength) | Defines the arrowhead length for the start of a stroke. |
| [getStartArrowType()](#getStartArrowType) | Defines the arrowhead for the start of a stroke. |
| [getStartArrowWidth()](#getStartArrowWidth) | Defines the arrowhead width for the start of a stroke. |
| [getTransparency()](#getTransparency) | Gets a value between 0.0 (opaque) and 1.0 (clear) representing the degree of transparency of the stroke. |
| [getVisible()](#getVisible) | Gets a flag indicating whether the stroke is visible. |
| [getWeight()](#getWeight) | Defines the brush thickness that strokes the path of a shape in points. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setBackColor(Color value)](#setBackColor-java.awt.Color) | Sets the background color of the stroke. |
| [setColor(Color value)](#setColor-java.awt.Color) | Defines the color of a stroke. |
| [setColor2(Color value)](#setColor2-java.awt.Color) | Defines a second color for a stroke. |
| [setDashStyle(int value)](#setDashStyle-int) | Specifies the dot and dash pattern for a stroke. |
| [setEndArrowLength(int value)](#setEndArrowLength-int) | Defines the arrowhead length for the end of a stroke. |
| [setEndArrowType(int value)](#setEndArrowType-int) | Defines the arrowhead for the end of a stroke. |
| [setEndArrowWidth(int value)](#setEndArrowWidth-int) | Defines the arrowhead width for the end of a stroke. |
| [setEndCap(int value)](#setEndCap-int) | Defines the cap style for the end of a stroke. |
| [setForeColor(Color value)](#setForeColor-java.awt.Color) | Sets the foreground color of the stroke. |
| [setJoinStyle(int value)](#setJoinStyle-int) | Defines the join style of a polyline. |
| [setLineStyle(int value)](#setLineStyle-int) | Defines the line style of the stroke. |
| [setOn(boolean value)](#setOn-boolean) | Defines whether the path will be stroked. |
| [setOpacity(double value)](#setOpacity-double) | Defines the amount of transparency of a stroke. |
| [setStartArrowLength(int value)](#setStartArrowLength-int) | Defines the arrowhead length for the start of a stroke. |
| [setStartArrowType(int value)](#setStartArrowType-int) | Defines the arrowhead for the start of a stroke. |
| [setStartArrowWidth(int value)](#setStartArrowWidth-int) | Defines the arrowhead width for the start of a stroke. |
| [setTransparency(double value)](#setTransparency-double) | Sets a value between 0.0 (opaque) and 1.0 (clear) representing the degree of transparency of the stroke. |
| [setVisible(boolean value)](#setVisible-boolean) | Sets a flag indicating whether the stroke is visible. |
| [setWeight(double value)](#setWeight-double) | Defines the brush thickness that strokes the path of a shape in points. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
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
### getBackColor() {#getBackColor}
```
public Color getBackColor()
```


Gets the background color of the stroke. The default value for a [Shape](../../com.aspose.words/shape) is .

**Returns:**
java.awt.Color - The background color of the stroke.
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


Defines the color of a stroke.

The default value for a [Shape](../../com.aspose.words/shape) is .

**Returns:**
java.awt.Color - The corresponding java.awt.Color value.
### getColor2() {#getColor2}
```
public Color getColor2()
```


Defines a second color for a stroke.

The default value for a [Shape](../../com.aspose.words/shape) is .

**Returns:**
java.awt.Color - The corresponding java.awt.Color value.
### getDashStyle() {#getDashStyle}
```
public int getDashStyle()
```


Specifies the dot and dash pattern for a stroke.

The default value is [DashStyle.SOLID](../../com.aspose.words/dashstyle\#SOLID).

**Returns:**
int - The corresponding  int  value. The returned value is one of [DashStyle](../../com.aspose.words/dashstyle) constants.
### getEndArrowLength() {#getEndArrowLength}
```
public int getEndArrowLength()
```


Defines the arrowhead length for the end of a stroke.

The default value is [ArrowLength.MEDIUM](../../com.aspose.words/arrowlength\#MEDIUM).

**Returns:**
int - The corresponding  int  value. The returned value is one of [ArrowLength](../../com.aspose.words/arrowlength) constants.
### getEndArrowType() {#getEndArrowType}
```
public int getEndArrowType()
```


Defines the arrowhead for the end of a stroke.

The default value is [ArrowType.NONE](../../com.aspose.words/arrowtype\#NONE).

**Returns:**
int - The corresponding  int  value. The returned value is one of [ArrowType](../../com.aspose.words/arrowtype) constants.
### getEndArrowWidth() {#getEndArrowWidth}
```
public int getEndArrowWidth()
```


Defines the arrowhead width for the end of a stroke.

The default value is [ArrowWidth.MEDIUM](../../com.aspose.words/arrowwidth\#MEDIUM).

**Returns:**
int - The corresponding  int  value. The returned value is one of [ArrowWidth](../../com.aspose.words/arrowwidth) constants.
### getEndCap() {#getEndCap}
```
public int getEndCap()
```


Defines the cap style for the end of a stroke.

The default value is [EndCap.FLAT](../../com.aspose.words/endcap\#FLAT).

**Returns:**
int - The corresponding  int  value. The returned value is one of [EndCap](../../com.aspose.words/endcap) constants.
### getForeColor() {#getForeColor}
```
public Color getForeColor()
```


Gets the foreground color of the stroke. The default value for a [Shape](../../com.aspose.words/shape) is .

**Returns:**
java.awt.Color - The foreground color of the stroke.
### getImageBytes() {#getImageBytes}
```
public byte[] getImageBytes()
```


Defines the image for a stroke image or pattern fill.

**Returns:**
byte[] - The corresponding byte[] value.
### getJoinStyle() {#getJoinStyle}
```
public int getJoinStyle()
```


Defines the join style of a polyline.

The default value is [JoinStyle.ROUND](../../com.aspose.words/joinstyle\#ROUND).

**Returns:**
int - The corresponding  int  value. The returned value is one of [JoinStyle](../../com.aspose.words/joinstyle) constants.
### getLineStyle() {#getLineStyle}
```
public int getLineStyle()
```


Defines the line style of the stroke.

The default value is [ShapeLineStyle.SINGLE](../../com.aspose.words/shapelinestyle\#SINGLE).

**Returns:**
int - The corresponding  int  value. The returned value is one of [ShapeLineStyle](../../com.aspose.words/shapelinestyle) constants.
### getOn() {#getOn}
```
public boolean getOn()
```


Defines whether the path will be stroked.

The default value for a [Shape](../../com.aspose.words/shape) is  true .

**Returns:**
boolean - The corresponding  boolean  value.
### getOpacity() {#getOpacity}
```
public double getOpacity()
```


Defines the amount of transparency of a stroke. Valid range is from 0 to 1.

The default value is 1.

**Returns:**
double - The corresponding  double  value.
### getStartArrowLength() {#getStartArrowLength}
```
public int getStartArrowLength()
```


Defines the arrowhead length for the start of a stroke.

The default value is [ArrowLength.MEDIUM](../../com.aspose.words/arrowlength\#MEDIUM).

**Returns:**
int - The corresponding  int  value. The returned value is one of [ArrowLength](../../com.aspose.words/arrowlength) constants.
### getStartArrowType() {#getStartArrowType}
```
public int getStartArrowType()
```


Defines the arrowhead for the start of a stroke.

The default value is [ArrowType.NONE](../../com.aspose.words/arrowtype\#NONE).

**Returns:**
int - The corresponding  int  value. The returned value is one of [ArrowType](../../com.aspose.words/arrowtype) constants.
### getStartArrowWidth() {#getStartArrowWidth}
```
public int getStartArrowWidth()
```


Defines the arrowhead width for the start of a stroke.

The default value is [ArrowWidth.MEDIUM](../../com.aspose.words/arrowwidth\#MEDIUM).

**Returns:**
int - The corresponding  int  value. The returned value is one of [ArrowWidth](../../com.aspose.words/arrowwidth) constants.
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


Gets a value between 0.0 (opaque) and 1.0 (clear) representing the degree of transparency of the stroke. The default value is 0.

**Returns:**
double - A value between 0.0 (opaque) and 1.0 (clear) representing the degree of transparency of the stroke.
### getVisible() {#getVisible}
```
public boolean getVisible()
```


Gets a flag indicating whether the stroke is visible. The default value for a [Shape](../../com.aspose.words/shape) is  true .

**Returns:**
boolean - A flag indicating whether the stroke is visible.
### getWeight() {#getWeight}
```
public double getWeight()
```


Defines the brush thickness that strokes the path of a shape in points.

The default value for a [Shape](../../com.aspose.words/shape) is 0.75.

**Returns:**
double - The corresponding  double  value.
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




### setBackColor(Color value) {#setBackColor-java.awt.Color}
```
public void setBackColor(Color value)
```


Sets the background color of the stroke. The default value for a [Shape](../../com.aspose.words/shape) is .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The background color of the stroke. |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Defines the color of a stroke.

The default value for a [Shape](../../com.aspose.words/shape) is .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The corresponding java.awt.Color value. |

### setColor2(Color value) {#setColor2-java.awt.Color}
```
public void setColor2(Color value)
```


Defines a second color for a stroke.

The default value for a [Shape](../../com.aspose.words/shape) is .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The corresponding java.awt.Color value. |

### setDashStyle(int value) {#setDashStyle-int}
```
public void setDashStyle(int value)
```


Specifies the dot and dash pattern for a stroke.

The default value is [DashStyle.SOLID](../../com.aspose.words/dashstyle\#SOLID).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [DashStyle](../../com.aspose.words/dashstyle) constants. |

### setEndArrowLength(int value) {#setEndArrowLength-int}
```
public void setEndArrowLength(int value)
```


Defines the arrowhead length for the end of a stroke.

The default value is [ArrowLength.MEDIUM](../../com.aspose.words/arrowlength\#MEDIUM).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [ArrowLength](../../com.aspose.words/arrowlength) constants. |

### setEndArrowType(int value) {#setEndArrowType-int}
```
public void setEndArrowType(int value)
```


Defines the arrowhead for the end of a stroke.

The default value is [ArrowType.NONE](../../com.aspose.words/arrowtype\#NONE).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [ArrowType](../../com.aspose.words/arrowtype) constants. |

### setEndArrowWidth(int value) {#setEndArrowWidth-int}
```
public void setEndArrowWidth(int value)
```


Defines the arrowhead width for the end of a stroke.

The default value is [ArrowWidth.MEDIUM](../../com.aspose.words/arrowwidth\#MEDIUM).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [ArrowWidth](../../com.aspose.words/arrowwidth) constants. |

### setEndCap(int value) {#setEndCap-int}
```
public void setEndCap(int value)
```


Defines the cap style for the end of a stroke.

The default value is [EndCap.FLAT](../../com.aspose.words/endcap\#FLAT).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [EndCap](../../com.aspose.words/endcap) constants. |

### setForeColor(Color value) {#setForeColor-java.awt.Color}
```
public void setForeColor(Color value)
```


Sets the foreground color of the stroke. The default value for a [Shape](../../com.aspose.words/shape) is .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The foreground color of the stroke. |

### setJoinStyle(int value) {#setJoinStyle-int}
```
public void setJoinStyle(int value)
```


Defines the join style of a polyline.

The default value is [JoinStyle.ROUND](../../com.aspose.words/joinstyle\#ROUND).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [JoinStyle](../../com.aspose.words/joinstyle) constants. |

### setLineStyle(int value) {#setLineStyle-int}
```
public void setLineStyle(int value)
```


Defines the line style of the stroke.

The default value is [ShapeLineStyle.SINGLE](../../com.aspose.words/shapelinestyle\#SINGLE).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [ShapeLineStyle](../../com.aspose.words/shapelinestyle) constants. |

### setOn(boolean value) {#setOn-boolean}
```
public void setOn(boolean value)
```


Defines whether the path will be stroked.

The default value for a [Shape](../../com.aspose.words/shape) is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setOpacity(double value) {#setOpacity-double}
```
public void setOpacity(double value)
```


Defines the amount of transparency of a stroke. Valid range is from 0 to 1.

The default value is 1.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### setStartArrowLength(int value) {#setStartArrowLength-int}
```
public void setStartArrowLength(int value)
```


Defines the arrowhead length for the start of a stroke.

The default value is [ArrowLength.MEDIUM](../../com.aspose.words/arrowlength\#MEDIUM).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [ArrowLength](../../com.aspose.words/arrowlength) constants. |

### setStartArrowType(int value) {#setStartArrowType-int}
```
public void setStartArrowType(int value)
```


Defines the arrowhead for the start of a stroke.

The default value is [ArrowType.NONE](../../com.aspose.words/arrowtype\#NONE).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [ArrowType](../../com.aspose.words/arrowtype) constants. |

### setStartArrowWidth(int value) {#setStartArrowWidth-int}
```
public void setStartArrowWidth(int value)
```


Defines the arrowhead width for the start of a stroke.

The default value is [ArrowWidth.MEDIUM](../../com.aspose.words/arrowwidth\#MEDIUM).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [ArrowWidth](../../com.aspose.words/arrowwidth) constants. |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


Sets a value between 0.0 (opaque) and 1.0 (clear) representing the degree of transparency of the stroke. The default value is 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | A value between 0.0 (opaque) and 1.0 (clear) representing the degree of transparency of the stroke. |

### setVisible(boolean value) {#setVisible-boolean}
```
public void setVisible(boolean value)
```


Sets a flag indicating whether the stroke is visible. The default value for a [Shape](../../com.aspose.words/shape) is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether the stroke is visible. |

### setWeight(double value) {#setWeight-double}
```
public void setWeight(double value)
```


Defines the brush thickness that strokes the path of a shape in points.

The default value for a [Shape](../../com.aspose.words/shape) is 0.75.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

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

