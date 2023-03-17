---
title: Fill
linktitle: Fill
second_title: Aspose.Words for Java API Reference
description: Represents fill formatting for an object in Java.
type: docs
weight: 269
url: /java/com.aspose.words/fill/
---

**Inheritance:**
java.lang.Object
```
public class Fill
```

Represents fill formatting for an object.

To learn more, visit the [ Working with Graphic Elements ][Working with Graphic Elements] documentation article.

Use the [ShapeBase.getFill()](../../com.aspose.words/shapebase/\#getFill) or [Font.getFill()](../../com.aspose.words/font/\#getFill) property to access fill properties of an object. You do not create instances of the [Fill](../../com.aspose.words/fill/) class directly.


[Working with Graphic Elements]: https://docs.aspose.com/words/java/working-with-graphic-elements/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getBackColor()](#getBackColor) | Gets a Color object that represents the background color for the fill. |
| [getBackThemeColor()](#getBackThemeColor) | Gets a ThemeColor object that represents the background color for the fill. |
| [getBackTintAndShade()](#getBackTintAndShade) | Gets a double value that lightens or darkens the background color. |
| [getClass()](#getClass) |  |
| [getColor()](#getColor) | Gets a Color object that represents the foreground color for the fill. |
| [getFillType()](#getFillType) | Gets a fill type. |
| [getForeColor()](#getForeColor) | Gets a Color object that represents the foreground color for the fill. |
| [getForeThemeColor()](#getForeThemeColor) | Gets a ThemeColor object that represents the foreground color for the fill. |
| [getForeTintAndShade()](#getForeTintAndShade) | Gets a double value that lightens or darkens the foreground color. |
| [getGradientAngle()](#getGradientAngle) | Gets the angle of the gradient fill. |
| [getGradientStops()](#getGradientStops) | Gets a collection of [GradientStop](../../com.aspose.words/gradientstop/) objects for the fill. |
| [getGradientStyle()](#getGradientStyle) | Gets the gradient style [GradientStyle](../../com.aspose.words/gradientstyle/) for the fill. |
| [getGradientVariant()](#getGradientVariant) | Gets the gradient variant [GradientVariant](../../com.aspose.words/gradientvariant/) for the fill. |
| [getImageBytes()](#getImageBytes) | Gets the raw bytes of the fill texture or pattern. |
| [getOn()](#getOn) | Gets value that is  true  if the formatting applied to this instance, is visible. |
| [getOpacity()](#getOpacity) | Gets the degree of opacity of the specified fill as a value between 0.0 (clear) and 1.0 (opaque). |
| [getPattern()](#getPattern) | Gets a [PatternType](../../com.aspose.words/patterntype/) for the fill. |
| [getPresetTexture()](#getPresetTexture) | Gets a [PresetTexture](../../com.aspose.words/presettexture/) for the fill. |
| [getRotateWithObject()](#getRotateWithObject) | Gets whether the fill rotates with the specified object. |
| [getTextureAlignment()](#getTextureAlignment) | Gets the alignment for tile texture fill. |
| [getTransparency()](#getTransparency) | Gets the degree of transparency of the specified fill as a value between 0.0 (opaque) and 1.0 (clear). |
| [getVisible()](#getVisible) | Gets value that is  true  if the formatting applied to this instance, is visible. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double) |  |
| [oneColorGradient(Color color, int style, int variant, double degree)](#oneColorGradient-java.awt.Color-int-int-double) |  |
| [patterned(int patternType)](#patterned-int) |  |
| [patterned(int patternType, Color foreColor, Color backColor)](#patterned-int-java.awt.Color-java.awt.Color) |  |
| [presetTextured(int presetTexture)](#presetTextured-int) |  |
| [setBackColor(Color value)](#setBackColor-java.awt.Color) | Sets a Color object that represents the background color for the fill. |
| [setBackThemeColor(int value)](#setBackThemeColor-int) | Sets a ThemeColor object that represents the background color for the fill. |
| [setBackTintAndShade(double value)](#setBackTintAndShade-double) | Sets a double value that lightens or darkens the background color. |
| [setColor(Color value)](#setColor-java.awt.Color) | Sets a Color object that represents the foreground color for the fill. |
| [setForeColor(Color value)](#setForeColor-java.awt.Color) | Sets a Color object that represents the foreground color for the fill. |
| [setForeThemeColor(int value)](#setForeThemeColor-int) | Sets a ThemeColor object that represents the foreground color for the fill. |
| [setForeTintAndShade(double value)](#setForeTintAndShade-double) | Sets a double value that lightens or darkens the foreground color. |
| [setGradientAngle(double value)](#setGradientAngle-double) | Sets the angle of the gradient fill. |
| [setImage(byte[] imageBytes)](#setImage-byte) | Changes the fill type to single image. |
| [setImage(InputStream stream)](#setImage-java.io.InputStream) |  |
| [setImage(String fileName)](#setImage-java.lang.String) | Changes the fill type to single image. |
| [setOn(boolean value)](#setOn-boolean) | Sets value that is  true  if the formatting applied to this instance, is visible. |
| [setOpacity(double value)](#setOpacity-double) | Sets the degree of opacity of the specified fill as a value between 0.0 (clear) and 1.0 (opaque). |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean) | Sets whether the fill rotates with the specified object. |
| [setTextureAlignment(int value)](#setTextureAlignment-int) | Sets the alignment for tile texture fill. |
| [setTransparency(double value)](#setTransparency-double) | Sets the degree of transparency of the specified fill as a value between 0.0 (opaque) and 1.0 (clear). |
| [setVisible(boolean value)](#setVisible-boolean) | Sets value that is  true  if the formatting applied to this instance, is visible. |
| [solid()](#solid) | Sets the fill to a uniform color. |
| [solid(Color color)](#solid-java.awt.Color) | Sets the fill to a specified uniform color. |
| [toString()](#toString) |  |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int) |  |
| [twoColorGradient(Color color1, Color color2, int style, int variant)](#twoColorGradient-java.awt.Color-java.awt.Color-int-int) |  |
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


Gets a Color object that represents the background color for the fill.

**Returns:**
java.awt.Color - A Color object that represents the background color for the fill.
### getBackThemeColor() {#getBackThemeColor}
```
public int getBackThemeColor()
```


Gets a ThemeColor object that represents the background color for the fill.

**Returns:**
int - A ThemeColor object that represents the background color for the fill. The returned value is one of [ThemeColor](../../com.aspose.words/themecolor/) constants.
### getBackTintAndShade() {#getBackTintAndShade}
```
public double getBackTintAndShade()
```


Gets a double value that lightens or darkens the background color.

The allowed values are within the range from -1 (the darkest) to 1 (the lightest) for this property. Zero (0) is neutral. Attempting to set this property to a value less than -1 or more than 1 results in java.lang.IllegalArgumentException.

**Returns:**
double - A double value that lightens or darkens the background color.
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


Gets a Color object that represents the foreground color for the fill.

**Returns:**
java.awt.Color - A Color object that represents the foreground color for the fill.
### getFillType() {#getFillType}
```
public int getFillType()
```


Gets a fill type.

**Returns:**
int - A fill type. The returned value is one of [FillType](../../com.aspose.words/filltype/) constants.
### getForeColor() {#getForeColor}
```
public Color getForeColor()
```


Gets a Color object that represents the foreground color for the fill.

**Returns:**
java.awt.Color - A Color object that represents the foreground color for the fill.
### getForeThemeColor() {#getForeThemeColor}
```
public int getForeThemeColor()
```


Gets a ThemeColor object that represents the foreground color for the fill.

**Returns:**
int - A ThemeColor object that represents the foreground color for the fill. The returned value is one of [ThemeColor](../../com.aspose.words/themecolor/) constants.
### getForeTintAndShade() {#getForeTintAndShade}
```
public double getForeTintAndShade()
```


Gets a double value that lightens or darkens the foreground color.

The allowed values are within the range from -1 (the darkest) to 1 (the lightest) for this property. Zero (0) is neutral. Attempting to set this property to a value less than -1 or more than 1 results in java.lang.IllegalArgumentException.

**Returns:**
double - A double value that lightens or darkens the foreground color.
### getGradientAngle() {#getGradientAngle}
```
public double getGradientAngle()
```


Gets the angle of the gradient fill.

**Returns:**
double - The angle of the gradient fill.
### getGradientStops() {#getGradientStops}
```
public GradientStopCollection getGradientStops()
```


Gets a collection of [GradientStop](../../com.aspose.words/gradientstop/) objects for the fill.

**Returns:**
[GradientStopCollection](../../com.aspose.words/gradientstopcollection/) - A collection of [GradientStop](../../com.aspose.words/gradientstop/) objects for the fill.
### getGradientStyle() {#getGradientStyle}
```
public int getGradientStyle()
```


Gets the gradient style [GradientStyle](../../com.aspose.words/gradientstyle/) for the fill.

**Returns:**
int - The gradient style [GradientStyle](../../com.aspose.words/gradientstyle/) for the fill. The returned value is one of [GradientStyle](../../com.aspose.words/gradientstyle/) constants.
### getGradientVariant() {#getGradientVariant}
```
public int getGradientVariant()
```


Gets the gradient variant [GradientVariant](../../com.aspose.words/gradientvariant/) for the fill.

**Returns:**
int - The gradient variant [GradientVariant](../../com.aspose.words/gradientvariant/) for the fill. The returned value is one of [GradientVariant](../../com.aspose.words/gradientvariant/) constants.
### getImageBytes() {#getImageBytes}
```
public byte[] getImageBytes()
```


Gets the raw bytes of the fill texture or pattern.

The default value is  null .

**Returns:**
byte[] - The raw bytes of the fill texture or pattern.
### getOn() {#getOn}
```
public boolean getOn()
```


Gets value that is  true  if the formatting applied to this instance, is visible.

**Returns:**
boolean - Value that is  true  if the formatting applied to this instance, is visible.
### getOpacity() {#getOpacity}
```
public double getOpacity()
```


Gets the degree of opacity of the specified fill as a value between 0.0 (clear) and 1.0 (opaque). This property is the opposite of property [getTransparency()](../../com.aspose.words/fill/\#getTransparency) / [setTransparency(double)](../../com.aspose.words/fill/\#setTransparency-double).

**Returns:**
double - The degree of opacity of the specified fill as a value between 0.0 (clear) and 1.0 (opaque).
### getPattern() {#getPattern}
```
public int getPattern()
```


Gets a [PatternType](../../com.aspose.words/patterntype/) for the fill.

**Returns:**
int - A [PatternType](../../com.aspose.words/patterntype/) for the fill. The returned value is one of [PatternType](../../com.aspose.words/patterntype/) constants.
### getPresetTexture() {#getPresetTexture}
```
public int getPresetTexture()
```


Gets a [PresetTexture](../../com.aspose.words/presettexture/) for the fill.

**Returns:**
int - A [PresetTexture](../../com.aspose.words/presettexture/) for the fill. The returned value is one of [PresetTexture](../../com.aspose.words/presettexture/) constants.
### getRotateWithObject() {#getRotateWithObject}
```
public boolean getRotateWithObject()
```


Gets whether the fill rotates with the specified object.

**Returns:**
boolean - Whether the fill rotates with the specified object.
### getTextureAlignment() {#getTextureAlignment}
```
public int getTextureAlignment()
```


Gets the alignment for tile texture fill.

**Returns:**
int - The alignment for tile texture fill. The returned value is one of [TextureAlignment](../../com.aspose.words/texturealignment/) constants.
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


Gets the degree of transparency of the specified fill as a value between 0.0 (opaque) and 1.0 (clear). This property is the opposite of property [getOpacity()](../../com.aspose.words/fill/\#getOpacity) / [setOpacity(double)](../../com.aspose.words/fill/\#setOpacity-double).

**Returns:**
double - The degree of transparency of the specified fill as a value between 0.0 (opaque) and 1.0 (clear).
### getVisible() {#getVisible}
```
public boolean getVisible()
```


Gets value that is  true  if the formatting applied to this instance, is visible.

**Returns:**
boolean - Value that is  true  if the formatting applied to this instance, is visible.
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




### oneColorGradient(int style, int variant, double degree) {#oneColorGradient-int-int-double}
```
public void oneColorGradient(int style, int variant, double degree)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| style | int |  |
| variant | int |  |
| degree | double |  |

### oneColorGradient(Color color, int style, int variant, double degree) {#oneColorGradient-java.awt.Color-int-int-double}
```
public void oneColorGradient(Color color, int style, int variant, double degree)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| color | java.awt.Color |  |
| style | int |  |
| variant | int |  |
| degree | double |  |

### patterned(int patternType) {#patterned-int}
```
public void patterned(int patternType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| patternType | int |  |

### patterned(int patternType, Color foreColor, Color backColor) {#patterned-int-java.awt.Color-java.awt.Color}
```
public void patterned(int patternType, Color foreColor, Color backColor)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| patternType | int |  |
| foreColor | java.awt.Color |  |
| backColor | java.awt.Color |  |

### presetTextured(int presetTexture) {#presetTextured-int}
```
public void presetTextured(int presetTexture)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| presetTexture | int |  |

### setBackColor(Color value) {#setBackColor-java.awt.Color}
```
public void setBackColor(Color value)
```


Sets a Color object that represents the background color for the fill.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | A Color object that represents the background color for the fill. |

### setBackThemeColor(int value) {#setBackThemeColor-int}
```
public void setBackThemeColor(int value)
```


Sets a ThemeColor object that represents the background color for the fill.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A ThemeColor object that represents the background color for the fill. The value must be one of [ThemeColor](../../com.aspose.words/themecolor/) constants. |

### setBackTintAndShade(double value) {#setBackTintAndShade-double}
```
public void setBackTintAndShade(double value)
```


Sets a double value that lightens or darkens the background color.

The allowed values are within the range from -1 (the darkest) to 1 (the lightest) for this property. Zero (0) is neutral. Attempting to set this property to a value less than -1 or more than 1 results in java.lang.IllegalArgumentException.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | A double value that lightens or darkens the background color. |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Sets a Color object that represents the foreground color for the fill.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | A Color object that represents the foreground color for the fill. |

### setForeColor(Color value) {#setForeColor-java.awt.Color}
```
public void setForeColor(Color value)
```


Sets a Color object that represents the foreground color for the fill.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | A Color object that represents the foreground color for the fill. |

### setForeThemeColor(int value) {#setForeThemeColor-int}
```
public void setForeThemeColor(int value)
```


Sets a ThemeColor object that represents the foreground color for the fill.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A ThemeColor object that represents the foreground color for the fill. The value must be one of [ThemeColor](../../com.aspose.words/themecolor/) constants. |

### setForeTintAndShade(double value) {#setForeTintAndShade-double}
```
public void setForeTintAndShade(double value)
```


Sets a double value that lightens or darkens the foreground color.

The allowed values are within the range from -1 (the darkest) to 1 (the lightest) for this property. Zero (0) is neutral. Attempting to set this property to a value less than -1 or more than 1 results in java.lang.IllegalArgumentException.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | A double value that lightens or darkens the foreground color. |

### setGradientAngle(double value) {#setGradientAngle-double}
```
public void setGradientAngle(double value)
```


Sets the angle of the gradient fill.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The angle of the gradient fill. |

### setImage(byte[] imageBytes) {#setImage-byte}
```
public void setImage(byte[] imageBytes)
```


Changes the fill type to single image.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | byte[] | The image bytes array. |

### setImage(InputStream stream) {#setImage-java.io.InputStream}
```
public void setImage(InputStream stream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### setImage(String fileName) {#setImage-java.lang.String}
```
public void setImage(String fileName)
```


Changes the fill type to single image.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The path to the image file. |

### setOn(boolean value) {#setOn-boolean}
```
public void setOn(boolean value)
```


Sets value that is  true  if the formatting applied to this instance, is visible.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Value that is  true  if the formatting applied to this instance, is visible. |

### setOpacity(double value) {#setOpacity-double}
```
public void setOpacity(double value)
```


Sets the degree of opacity of the specified fill as a value between 0.0 (clear) and 1.0 (opaque). This property is the opposite of property [getTransparency()](../../com.aspose.words/fill/\#getTransparency) / [setTransparency(double)](../../com.aspose.words/fill/\#setTransparency-double).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The degree of opacity of the specified fill as a value between 0.0 (clear) and 1.0 (opaque). |

### setRotateWithObject(boolean value) {#setRotateWithObject-boolean}
```
public void setRotateWithObject(boolean value)
```


Sets whether the fill rotates with the specified object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether the fill rotates with the specified object. |

### setTextureAlignment(int value) {#setTextureAlignment-int}
```
public void setTextureAlignment(int value)
```


Sets the alignment for tile texture fill.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The alignment for tile texture fill. The value must be one of [TextureAlignment](../../com.aspose.words/texturealignment/) constants. |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


Sets the degree of transparency of the specified fill as a value between 0.0 (opaque) and 1.0 (clear). This property is the opposite of property [getOpacity()](../../com.aspose.words/fill/\#getOpacity) / [setOpacity(double)](../../com.aspose.words/fill/\#setOpacity-double).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The degree of transparency of the specified fill as a value between 0.0 (opaque) and 1.0 (clear). |

### setVisible(boolean value) {#setVisible-boolean}
```
public void setVisible(boolean value)
```


Sets value that is  true  if the formatting applied to this instance, is visible.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Value that is  true  if the formatting applied to this instance, is visible. |

### solid() {#solid}
```
public void solid()
```


Sets the fill to a uniform color. Use this method to convert any of the fills back to solid fill.

### solid(Color color) {#solid-java.awt.Color}
```
public void solid(Color color)
```


Sets the fill to a specified uniform color. Use this method to convert any of the fills back to solid fill.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| color | java.awt.Color |  |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### twoColorGradient(int style, int variant) {#twoColorGradient-int-int}
```
public void twoColorGradient(int style, int variant)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| style | int |  |
| variant | int |  |

### twoColorGradient(Color color1, Color color2, int style, int variant) {#twoColorGradient-java.awt.Color-java.awt.Color-int-int}
```
public void twoColorGradient(Color color1, Color color2, int style, int variant)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| color1 | java.awt.Color |  |
| color2 | java.awt.Color |  |
| style | int |  |
| variant | int |  |

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

