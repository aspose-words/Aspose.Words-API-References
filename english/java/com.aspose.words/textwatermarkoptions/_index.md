---
title: TextWatermarkOptions
second_title: Aspose.Words for Java API Reference
description: Contains options that can be specified when adding a watermark with text.
type: docs
weight: 572
url: /java/com.aspose.words/textwatermarkoptions/
---

**Inheritance:**
java.lang.Object
```
public class TextWatermarkOptions
```

Contains options that can be specified when adding a watermark with text.

To learn more, visit the [ Working with Watermark ][Working with Watermark] documentation article.


[Working with Watermark]: https://docs.aspose.com/words/java/working-with-watermark/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getColor()](#getColor) | Gets font color. |
| [getFontFamily()](#getFontFamily) | Gets font family name. |
| [getFontSize()](#getFontSize) | Gets a font size. |
| [getLayout()](#getLayout) | Gets layout of the watermark. |
| [hashCode()](#hashCode) |  |
| [isSemitrasparent()](#isSemitrasparent) | Gets a boolean value which is responsible for opacity of the watermark. |
| [isSemitrasparent(boolean value)](#isSemitrasparent-boolean) | Sets a boolean value which is responsible for opacity of the watermark. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setColor(Color value)](#setColor-java.awt.Color) | Sets font color. |
| [setFontFamily(String value)](#setFontFamily-java.lang.String) | Sets font family name. |
| [setFontSize(float value)](#setFontSize-float) | Sets a font size. |
| [setLayout(int value)](#setLayout-int) | Sets layout of the watermark. |
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


Gets font color. The default value is java.awt.Color\#getSilver().getSilver().

**Returns:**
java.awt.Color - Font color.
### getFontFamily() {#getFontFamily}
```
public String getFontFamily()
```


Gets font family name. The default value is "Calibri".

**Returns:**
java.lang.String - Font family name.
### getFontSize() {#getFontSize}
```
public float getFontSize()
```


Gets a font size. The default value is 0 - auto.

Valid values range from 0 to 65.5 inclusive.

Auto font size means that the watermark will be scaled to its max width and max height relative to the page margins.

**Returns:**
float - A font size.
### getLayout() {#getLayout}
```
public int getLayout()
```


Gets layout of the watermark. The default value is [WatermarkLayout.DIAGONAL](../../com.aspose.words/watermarklayout\#DIAGONAL).

**Returns:**
int - Layout of the watermark. The returned value is one of [WatermarkLayout](../../com.aspose.words/watermarklayout) constants.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isSemitrasparent() {#isSemitrasparent}
```
public boolean isSemitrasparent()
```


Gets a boolean value which is responsible for opacity of the watermark. The default value is  true .

**Returns:**
boolean - A boolean value which is responsible for opacity of the watermark.
### isSemitrasparent(boolean value) {#isSemitrasparent-boolean}
```
public void isSemitrasparent(boolean value)
```


Sets a boolean value which is responsible for opacity of the watermark. The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value which is responsible for opacity of the watermark. |

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


Sets font color. The default value is java.awt.Color\#getSilver().getSilver().

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | Font color. |

### setFontFamily(String value) {#setFontFamily-java.lang.String}
```
public void setFontFamily(String value)
```


Sets font family name. The default value is "Calibri".

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Font family name. |

### setFontSize(float value) {#setFontSize-float}
```
public void setFontSize(float value)
```


Sets a font size. The default value is 0 - auto.

Valid values range from 0 to 65.5 inclusive.

Auto font size means that the watermark will be scaled to its max width and max height relative to the page margins.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | float | A font size. |

### setLayout(int value) {#setLayout-int}
```
public void setLayout(int value)
```


Sets layout of the watermark. The default value is [WatermarkLayout.DIAGONAL](../../com.aspose.words/watermarklayout\#DIAGONAL).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Layout of the watermark. The value must be one of [WatermarkLayout](../../com.aspose.words/watermarklayout) constants. |

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

