---
title: BorderCollection
second_title: Aspose.Words for Java API Reference
description: A collection of  objects.
type: docs
weight: 37
url: /java/com.aspose.words/bordercollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class BorderCollection implements Iterable
```

A collection of [Border](../../com.aspose.words/border) objects.

To learn more, visit the [ Programming with Documents ][Programming with Documents] documentation article.

Different document elements have different borders. For example, [ParagraphFormat](../../com.aspose.words/paragraphformat) has [getBottom()](../../com.aspose.words/bordercollection\#getBottom), [getLeft()](../../com.aspose.words/bordercollection\#getLeft), [getRight()](../../com.aspose.words/bordercollection\#getRight) and [getTop()](../../com.aspose.words/bordercollection\#getTop) borders. You can specify different formatting for each border independently or enumerate through all borders and apply same formatting.


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Methods

| Method | Description |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Removes all borders of an object. |
| [equals(BorderCollection brColl)](#equals-com.aspose.words.BorderCollection) | Compares collections of borders. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [get(int index)](#get-int) | Retrieves a [Border](../../com.aspose.words/border) object by index. |
| [getBottom()](#getBottom) | Gets the bottom border. |
| [getByBorderType(int borderType)](#getByBorderType-int) |  |
| [getClass()](#getClass) |  |
| [getColor()](#getColor) | Gets the border color. |
| [getCount()](#getCount) | Gets the number of borders in the collection. |
| [getDistanceFromText()](#getDistanceFromText) | Gets distance of the border from text in points. |
| [getHorizontal()](#getHorizontal) | Gets the horizontal border that is used between cells or conforming paragraphs. |
| [getLeft()](#getLeft) | Gets the left border. |
| [getLineStyle()](#getLineStyle) | Gets the border style. |
| [getLineWidth()](#getLineWidth) | Gets the border width in points. |
| [getRight()](#getRight) | Gets the right border. |
| [getShadow()](#getShadow) | Gets a value indicating whether the border has a shadow. |
| [getTop()](#getTop) | Gets the top border. |
| [getVertical()](#getVertical) | Gets the vertical border that is used between cells. |
| [hashCode()](#hashCode) |  |
| [iterator()](#iterator) | Returns an enumerator object that can be used to iterate over all borders in the collection. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setColor(Color value)](#setColor-java.awt.Color) | Sets the border color. |
| [setDistanceFromText(double value)](#setDistanceFromText-double) | Sets distance of the border from text in points. |
| [setLineStyle(int value)](#setLineStyle-int) | Sets the border style. |
| [setLineWidth(double value)](#setLineWidth-double) | Sets the border width in points. |
| [setShadow(boolean value)](#setShadow-boolean) | Sets a value indicating whether the border has a shadow. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Removes all borders of an object.

### equals(BorderCollection brColl) {#equals-com.aspose.words.BorderCollection}
```
public boolean equals(BorderCollection brColl)
```


Compares collections of borders.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| brColl | [BorderCollection](../../com.aspose.words/bordercollection) |  |

**Returns:**
boolean
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
### get(int index) {#get-int}
```
public Border get(int index)
```


Retrieves a [Border](../../com.aspose.words/border) object by index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the border to retrieve. |

**Returns:**
[Border](../../com.aspose.words/border) - The corresponding [Border](../../com.aspose.words/border) value.
### getBottom() {#getBottom}
```
public Border getBottom()
```


Gets the bottom border.

**Returns:**
[Border](../../com.aspose.words/border) - The bottom border.
### getByBorderType(int borderType) {#getByBorderType-int}
```
public Border getByBorderType(int borderType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| borderType | int |  |

**Returns:**
[Border](../../com.aspose.words/border)
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

Returns the color of the first border in the collection.

Sets the color of all borders in the collection excluding diagonal borders.

**Returns:**
java.awt.Color - The border color.
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of borders in the collection.

**Returns:**
int - The number of borders in the collection.
### getDistanceFromText() {#getDistanceFromText}
```
public double getDistanceFromText()
```


Gets distance of the border from text in points.

Gets the distance from text for the first border.

Sets the distance from text for all borders in the collection excluding diagonal borders.

Has no effect and will be automatically reset to zero for borders of table cells.

**Returns:**
double - Distance of the border from text in points.
### getHorizontal() {#getHorizontal}
```
public Border getHorizontal()
```


Gets the horizontal border that is used between cells or conforming paragraphs.

**Returns:**
[Border](../../com.aspose.words/border) - The horizontal border that is used between cells or conforming paragraphs.
### getLeft() {#getLeft}
```
public Border getLeft()
```


Gets the left border.

**Returns:**
[Border](../../com.aspose.words/border) - The left border.
### getLineStyle() {#getLineStyle}
```
public int getLineStyle()
```


Gets the border style.

Returns the style of the first border in the collection.

Sets the style of all borders in the collection excluding diagonal borders.

**Returns:**
int - The border style. The returned value is one of [LineStyle](../../com.aspose.words/linestyle) constants.
### getLineWidth() {#getLineWidth}
```
public double getLineWidth()
```


Gets the border width in points.

Returns the width of the first border in the collection.

Sets the width of all borders in the collection excluding diagonal borders.

**Returns:**
double - The border width in points.
### getRight() {#getRight}
```
public Border getRight()
```


Gets the right border.

**Returns:**
[Border](../../com.aspose.words/border) - The right border.
### getShadow() {#getShadow}
```
public boolean getShadow()
```


Gets a value indicating whether the border has a shadow.

Gets the value from the first border in the collection.

Sets the value for all borders in the collection excluding diagonal borders.

**Returns:**
boolean - A value indicating whether the border has a shadow.
### getTop() {#getTop}
```
public Border getTop()
```


Gets the top border.

**Returns:**
[Border](../../com.aspose.words/border) - The top border.
### getVertical() {#getVertical}
```
public Border getVertical()
```


Gets the vertical border that is used between cells.

**Returns:**
[Border](../../com.aspose.words/border) - The vertical border that is used between cells.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### iterator() {#iterator}
```
public Iterator iterator()
```


Returns an enumerator object that can be used to iterate over all borders in the collection.

**Returns:**
java.util.Iterator
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

Returns the color of the first border in the collection.

Sets the color of all borders in the collection excluding diagonal borders.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The border color. |

### setDistanceFromText(double value) {#setDistanceFromText-double}
```
public void setDistanceFromText(double value)
```


Sets distance of the border from text in points.

Gets the distance from text for the first border.

Sets the distance from text for all borders in the collection excluding diagonal borders.

Has no effect and will be automatically reset to zero for borders of table cells.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | Distance of the border from text in points. |

### setLineStyle(int value) {#setLineStyle-int}
```
public void setLineStyle(int value)
```


Sets the border style.

Returns the style of the first border in the collection.

Sets the style of all borders in the collection excluding diagonal borders.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The border style. The value must be one of [LineStyle](../../com.aspose.words/linestyle) constants. |

### setLineWidth(double value) {#setLineWidth-double}
```
public void setLineWidth(double value)
```


Sets the border width in points.

Returns the width of the first border in the collection.

Sets the width of all borders in the collection excluding diagonal borders.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The border width in points. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


Sets a value indicating whether the border has a shadow.

Gets the value from the first border in the collection.

Sets the value for all borders in the collection excluding diagonal borders.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether the border has a shadow. |

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

