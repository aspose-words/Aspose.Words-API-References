---
title: Shading
linktitle: Shading
second_title: Aspose.Words for Java API Reference
description: Contains shading attributes for an object in Java.
type: docs
weight: 519
url: /java/com.aspose.words/shading/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Shading extends InternableComplexAttr implements Cloneable
```

Contains shading attributes for an object.

To learn more, visit the [ Programming with Documents ][Programming with Documents] documentation article.


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Methods

| Method | Description |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Removes shading from the object. |
| [equals(Shading rhs)](#equals-com.aspose.words.Shading) | Determines whether the specified [Shading](../../com.aspose.words/shading/) is equal in value to the current [Shading](../../com.aspose.words/shading/). |
| [equals(Object obj)](#equals-java.lang.Object) | Determines whether the specified object is equal in value to the current object. |
| [getBackgroundPatternColor()](#getBackgroundPatternColor) | Gets the color that's applied to the background of the [Shading](../../com.aspose.words/shading/) object. |
| [getBackgroundPatternThemeColor()](#getBackgroundPatternThemeColor) | Gets the background pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object. |
| [getBackgroundTintAndShade()](#getBackgroundTintAndShade) | Gets a double value that lightens or darkens a background theme color. |
| [getClass()](#getClass) |  |
| [getForegroundPatternColor()](#getForegroundPatternColor) | Gets the color that's applied to the foreground of the [Shading](../../com.aspose.words/shading/) object. |
| [getForegroundPatternThemeColor()](#getForegroundPatternThemeColor) | Gets the foreground pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object. |
| [getForegroundTintAndShade()](#getForegroundTintAndShade) | Gets a double value that lightens or darkens a foreground theme color. |
| [getTexture()](#getTexture) | Gets the shading texture. |
| [hashCode()](#hashCode) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setBackgroundPatternColor(Color value)](#setBackgroundPatternColor-java.awt.Color) | Sets the color that's applied to the background of the [Shading](../../com.aspose.words/shading/) object. |
| [setBackgroundPatternThemeColor(int value)](#setBackgroundPatternThemeColor-int) | Sets the background pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object. |
| [setBackgroundTintAndShade(double value)](#setBackgroundTintAndShade-double) | Sets a double value that lightens or darkens a background theme color. |
| [setForegroundPatternColor(Color value)](#setForegroundPatternColor-java.awt.Color) | Sets the color that's applied to the foreground of the [Shading](../../com.aspose.words/shading/) object. |
| [setForegroundPatternThemeColor(int value)](#setForegroundPatternThemeColor-int) | Sets the foreground pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object. |
| [setForegroundTintAndShade(double value)](#setForegroundTintAndShade-double) | Sets a double value that lightens or darkens a foreground theme color. |
| [setTexture(int value)](#setTexture-int) | Sets the shading texture. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Removes shading from the object.

### equals(Shading rhs) {#equals-com.aspose.words.Shading}
```
public boolean equals(Shading rhs)
```


Determines whether the specified [Shading](../../com.aspose.words/shading/) is equal in value to the current [Shading](../../com.aspose.words/shading/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rhs | [Shading](../../com.aspose.words/shading/) |  |

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
### getBackgroundPatternColor() {#getBackgroundPatternColor}
```
public Color getBackgroundPatternColor()
```


Gets the color that's applied to the background of the [Shading](../../com.aspose.words/shading/) object.

**Returns:**
java.awt.Color - The color that's applied to the background of the [Shading](../../com.aspose.words/shading/) object.
### getBackgroundPatternThemeColor() {#getBackgroundPatternThemeColor}
```
public int getBackgroundPatternThemeColor()
```


Gets the background pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object.

**Returns:**
int - The background pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object. The returned value is one of [ThemeColor](../../com.aspose.words/themecolor/) constants.
### getBackgroundTintAndShade() {#getBackgroundTintAndShade}
```
public double getBackgroundTintAndShade()
```


Gets a double value that lightens or darkens a background theme color.

The allowed values are in the range from -1 (the darkest) to 1 (the lightest) for this property. Zero (0) is neutral. Attempting to set this property to a value less than -1 or more than 1 results in java.lang.IllegalArgumentException.

Setting this property for Border object with non-theme colors results in java.lang.IllegalStateException.

**Returns:**
double - A double value that lightens or darkens a background theme color.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getForegroundPatternColor() {#getForegroundPatternColor}
```
public Color getForegroundPatternColor()
```


Gets the color that's applied to the foreground of the [Shading](../../com.aspose.words/shading/) object.

**Returns:**
java.awt.Color - The color that's applied to the foreground of the [Shading](../../com.aspose.words/shading/) object.
### getForegroundPatternThemeColor() {#getForegroundPatternThemeColor}
```
public int getForegroundPatternThemeColor()
```


Gets the foreground pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object.

**Returns:**
int - The foreground pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object. The returned value is one of [ThemeColor](../../com.aspose.words/themecolor/) constants.
### getForegroundTintAndShade() {#getForegroundTintAndShade}
```
public double getForegroundTintAndShade()
```


Gets a double value that lightens or darkens a foreground theme color.

The allowed values are in the range from -1 (the darkest) to 1 (the lightest) for this property. Zero (0) is neutral. Attempting to set this property to a value less than -1 or more than 1 results in java.lang.IllegalArgumentException.

Setting this property for Border object with non-theme colors results in java.lang.IllegalStateException.

**Returns:**
double - A double value that lightens or darkens a foreground theme color.
### getTexture() {#getTexture}
```
public int getTexture()
```


Gets the shading texture.

**Returns:**
int - The shading texture. The returned value is one of [TextureIndex](../../com.aspose.words/textureindex/) constants.
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
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### setBackgroundPatternColor(Color value) {#setBackgroundPatternColor-java.awt.Color}
```
public void setBackgroundPatternColor(Color value)
```


Sets the color that's applied to the background of the [Shading](../../com.aspose.words/shading/) object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The color that's applied to the background of the [Shading](../../com.aspose.words/shading/) object. |

### setBackgroundPatternThemeColor(int value) {#setBackgroundPatternThemeColor-int}
```
public void setBackgroundPatternThemeColor(int value)
```


Sets the background pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The background pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object. The value must be one of [ThemeColor](../../com.aspose.words/themecolor/) constants. |

### setBackgroundTintAndShade(double value) {#setBackgroundTintAndShade-double}
```
public void setBackgroundTintAndShade(double value)
```


Sets a double value that lightens or darkens a background theme color.

The allowed values are in the range from -1 (the darkest) to 1 (the lightest) for this property. Zero (0) is neutral. Attempting to set this property to a value less than -1 or more than 1 results in java.lang.IllegalArgumentException.

Setting this property for Border object with non-theme colors results in java.lang.IllegalStateException.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | A double value that lightens or darkens a background theme color. |

### setForegroundPatternColor(Color value) {#setForegroundPatternColor-java.awt.Color}
```
public void setForegroundPatternColor(Color value)
```


Sets the color that's applied to the foreground of the [Shading](../../com.aspose.words/shading/) object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The color that's applied to the foreground of the [Shading](../../com.aspose.words/shading/) object. |

### setForegroundPatternThemeColor(int value) {#setForegroundPatternThemeColor-int}
```
public void setForegroundPatternThemeColor(int value)
```


Sets the foreground pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The foreground pattern theme color in the applied color scheme that is associated with this [Shading](../../com.aspose.words/shading/) object. The value must be one of [ThemeColor](../../com.aspose.words/themecolor/) constants. |

### setForegroundTintAndShade(double value) {#setForegroundTintAndShade-double}
```
public void setForegroundTintAndShade(double value)
```


Sets a double value that lightens or darkens a foreground theme color.

The allowed values are in the range from -1 (the darkest) to 1 (the lightest) for this property. Zero (0) is neutral. Attempting to set this property to a value less than -1 or more than 1 results in java.lang.IllegalArgumentException.

Setting this property for Border object with non-theme colors results in java.lang.IllegalStateException.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | A double value that lightens or darkens a foreground theme color. |

### setTexture(int value) {#setTexture-int}
```
public void setTexture(int value)
```


Sets the shading texture.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The shading texture. The value must be one of [TextureIndex](../../com.aspose.words/textureindex/) constants. |

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

