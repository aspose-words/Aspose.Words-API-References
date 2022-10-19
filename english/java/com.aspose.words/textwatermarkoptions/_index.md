---
title: TextWatermarkOptions
second_title: Aspose.Words for Java API Reference
description: Contains options that can be specified when adding a watermark with text.
type: docs
weight: 569
url: /java/com.aspose.words/textwatermarkoptions/
---

**Inheritance:**
java.lang.Object
```
public class TextWatermarkOptions
```

Contains options that can be specified when adding a watermark with text.

To learn more, visit the **Working with Watermark** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getFontFamily()](#getFontFamily--) | Gets font family name. |
| [setFontFamily(String value)](#setFontFamily-java.lang.String-) | Sets font family name. |
| [getColor()](#getColor--) | Gets font color. |
| [setColor(Color value)](#setColor-java.awt.Color-) | Sets font color. |
| [getFontSize()](#getFontSize--) | Gets a font size. |
| [setFontSize(float value)](#setFontSize-float-) | Sets a font size. |
| [isSemitrasparent()](#isSemitrasparent--) | Gets a boolean value which is responsible for opacity of the watermark. |
| [isSemitrasparent(boolean value)](#isSemitrasparent-boolean-) | Sets a boolean value which is responsible for opacity of the watermark. |
| [getLayout()](#getLayout--) | Gets layout of the watermark. |
| [setLayout(int value)](#setLayout-int-) | Sets layout of the watermark. |
### getFontFamily() {#getFontFamily--}
```
public String getFontFamily()
```


Gets font family name. The default value is "Calibri".

**Returns:**
java.lang.String - Font family name.
### setFontFamily(String value) {#setFontFamily-java.lang.String-}
```
public void setFontFamily(String value)
```


Sets font family name. The default value is "Calibri".

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Font family name. |

### getColor() {#getColor--}
```
public Color getColor()
```


Gets font color. The default value is Color.Silver.

**Returns:**
java.awt.Color - Font color.
### setColor(Color value) {#setColor-java.awt.Color-}
```
public void setColor(Color value)
```


Sets font color. The default value is Color.Silver.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | Font color. |

### getFontSize() {#getFontSize--}
```
public float getFontSize()
```


Gets a font size. The default value is 0 - auto.

Valid values range from 0 to 65.5 inclusive.

Auto font size means that the watermark will be scaled to its max width and max height relative to the page margins.

**Returns:**
float - A font size.
### setFontSize(float value) {#setFontSize-float-}
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

### isSemitrasparent() {#isSemitrasparent--}
```
public boolean isSemitrasparent()
```


Gets a boolean value which is responsible for opacity of the watermark. The default value is True.

**Returns:**
boolean - A boolean value which is responsible for opacity of the watermark.
### isSemitrasparent(boolean value) {#isSemitrasparent-boolean-}
```
public void isSemitrasparent(boolean value)
```


Sets a boolean value which is responsible for opacity of the watermark. The default value is True.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value which is responsible for opacity of the watermark. |

### getLayout() {#getLayout--}
```
public int getLayout()
```


Gets layout of the watermark. The default value is [WatermarkLayout.DIAGONAL](../../com.aspose.words/watermarklayout\#DIAGONAL).

**Returns:**
int - Layout of the watermark. The returned value is one of [WatermarkLayout](../../com.aspose.words/watermarklayout) constants.
### setLayout(int value) {#setLayout-int-}
```
public void setLayout(int value)
```


Sets layout of the watermark. The default value is [WatermarkLayout.DIAGONAL](../../com.aspose.words/watermarklayout\#DIAGONAL).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Layout of the watermark. The value must be one of [WatermarkLayout](../../com.aspose.words/watermarklayout) constants. |

