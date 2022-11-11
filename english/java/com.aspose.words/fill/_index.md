---
title: Fill
second_title: Aspose.Words for Java API 参考
description: 表示对象的填充格式。
type: docs
weight: 267
url: /zh/java/com.aspose.words/fill/
---

**遗产:**
java.lang.Object
```
public class Fill
```

表示对象的填充格式。

要了解更多信息，请访问**Working with Graphic Elements**文档文章。

使用[ShapeBase.getFill()](../../com.aspose.words/shapebase\#getFill--)或者[Font.getFill()](../../com.aspose.words/font\#getFill--)属性来访问对象的填充属性。您不创建的实例[Fill](../../com.aspose.words/fill)直接上课。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBackColor()](#getBackColor--) | 获取一个 Color 对象，该对象表示填充的背景色。 |
| [get班级()](#get班级--) |  |
| [getColor()](#getColor--) | 获取一个 Color 对象，该对象表示填充的前景色。 |
| [getFill类型()](#getFill类型--) | 获取填充类型。 |
| [getForeColor()](#getForeColor--) | 获取一个 Color 对象，该对象表示填充的前景色。 |
| [getGradientAngle()](#getGradientAngle--) | 获取渐变填充的角度。 |
| [getGradientStops()](#getGradientStops--) | 获取一个集合[GradientStop](../../com.aspose.words/gradientstop)填充对象。 |
| [getGradientStyle()](#getGradientStyle--) | 获取渐变样式[GradientStyle](../../com.aspose.words/gradientstyle)为填充。 |
| [getGradientVariant()](#getGradientVariant--) | 获取渐变变体[GradientVariant](../../com.aspose.words/gradientvariant)为填充。 |
| [getImageBytes()](#getImageBytes--) | 获取填充纹理或图案的原始字节。 |
| [getOn()](#getOn--) | 如果应用于此实例的格式可见，则获取值为 true。 |
| [getOpacity()](#getOpacity--) | 获取指定填充的不透明度，取值介于 0.0（透明）和 1.0（不透明）之间。 |
| [getPattern()](#getPattern--) | 得到一个[Pattern类型](../../com.aspose.words/patterntype)为填充。 |
| [getPresetTexture()](#getPresetTexture--) | 得到一个[PresetTexture](../../com.aspose.words/presettexture)为填充。 |
| [getRotateWithObject()](#getRotateWithObject--) | 获取填充是否随指定对象旋转。 |
| [getTextureAlignment()](#getTextureAlignment--) | 获取平铺纹理填充的对齐方式。 |
| [getTransparency()](#getTransparency--) | 获取指定填充的透明度，作为 0.0（不透明）和 1.0（透明）之间的值。 |
| [getVisible()](#getVisible--) | 如果应用于此实例的格式可见，则获取值为 true。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double-) |  |
| [oneColorGradient(Color color, int style, int variant, double degree)](#oneColorGradient-java.awt.Color-int-int-double-) |  |
| [patterned(int pattern类型)](#patterned-int-) |  |
| [patterned(int pattern类型, Color foreColor, Color backColor)](#patterned-int-java.awt.Color-java.awt.Color-) |  |
| [presetTextured(int presetTexture)](#presetTextured-int-) |  |
| [setBackColor(Color value)](#setBackColor-java.awt.Color-) | 设置表示填充背景颜色的 Color 对象。 |
| [setColor(Color value)](#setColor-java.awt.Color-) | 设置表示填充的前景色的 Color 对象。 |
| [setForeColor(Color value)](#setForeColor-java.awt.Color-) | 设置表示填充的前景色的 Color 对象。 |
| [setGradientAngle(double value)](#setGradientAngle-double-) | 设置渐变填充的角度。 |
| [setImage(byte[] imageBytes)](#setImage-byte---) | 将填充类型更改为单个图像。 |
| [setImage(InputStream stream)](#setImage-java.io.InputStream-) |  |
| [setImage(String fileName)](#setImage-java.lang.String-) | 将填充类型更改为单个图像。 |
| [setOn(boolean value)](#setOn-boolean-) | 如果应用于此实例的格式可见，则设置值为 true。 |
| [setOpacity(double value)](#setOpacity-double-) | 将指定填充的不透明度设置为 0.0（透明）和 1.0（不透明）之间的值。 |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean-) | 设置填充是否随指定对象旋转。 |
| [setTextureAlignment(int value)](#setTextureAlignment-int-) | 设置平铺纹理填充的对齐方式。 |
| [setTransparency(double value)](#setTransparency-double-) | 将指定填充的透明度设置为 0.0（不透明）和 1.0（透明）之间的值。 |
| [setVisible(boolean value)](#setVisible-boolean-) | 如果应用于此实例的格式可见，则设置值为 true。 |
| [solid()](#solid--) | 将填充设置为统一颜色。 |
| [solid(Color color)](#solid-java.awt.Color-) | 将填充设置为指定的统一颜色。 |
| [toString()](#toString--) |  |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int-) |  |
| [twoColorGradient(Color color1, Color color2, int style, int variant)](#twoColorGradient-java.awt.Color-java.awt.Color-int-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### getBackColor() {#getBackColor--}
```
public Color getBackColor()
```


获取一个 Color 对象，该对象表示填充的背景色。

**退货:**
java.awt.Color - 一个 Color 对象，表示填充的背景颜色。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getColor() {#getColor--}
```
public Color getColor()
```


获取一个 Color 对象，该对象表示填充的前景色。

**退货:**
java.awt.Color - 一个 Color 对象，表示填充的前景色。
### getFill类型() {#getFill类型--}
```
public int getFill类型()
```


获取填充类型。

**退货:**
 int - 一种填充类型。返回值是以下之一[Fill类型](../../com.aspose.words/filltype)常数。
### getForeColor() {#getForeColor--}
```
public Color getForeColor()
```


获取一个 Color 对象，该对象表示填充的前景色。

**退货:**
java.awt.Color - 一个 Color 对象，表示填充的前景色。
### getGradientAngle() {#getGradientAngle--}
```
public double getGradientAngle()
```


获取渐变填充的角度。

**退货:**
double - 渐变填充的角度。
### getGradientStops() {#getGradientStops--}
```
public GradientStopCollection getGradientStops()
```


获取一个集合[GradientStop](../../com.aspose.words/gradientstop)填充对象。

**退货:**
[GradientStopCollection](../../com.aspose.words/gradientstopcollection) - 集合[GradientStop](../../com.aspose.words/gradientstop)填充对象。
### getGradientStyle() {#getGradientStyle--}
```
public int getGradientStyle()
```


获取渐变样式[GradientStyle](../../com.aspose.words/gradientstyle)为填充。

**退货:**
 int - 渐变样式[GradientStyle](../../com.aspose.words/gradientstyle)为填充。返回值是以下之一[GradientStyle](../../com.aspose.words/gradientstyle)常数。
### getGradientVariant() {#getGradientVariant--}
```
public int getGradientVariant()
```


获取渐变变体[GradientVariant](../../com.aspose.words/gradientvariant)为填充。

**退货:**
int - 渐变变体[GradientVariant](../../com.aspose.words/gradientvariant)为填充。返回值是以下之一[GradientVariant](../../com.aspose.words/gradientvariant)常数。
### getImageBytes() {#getImageBytes--}
```
public byte[] getImageBytes()
```


获取填充纹理或图案的原始字节。

默认值为空。

**退货:**
字节[- 填充纹理或图案的原始字节。
### getOn() {#getOn--}
```
public boolean getOn()
```


如果应用于此实例的格式可见，则获取值为 true。

**退货:**
boolean - 如果应用于此实例的格式可见，则该值为 true。
### getOpacity() {#getOpacity--}
```
public double getOpacity()
```


获取指定填充的不透明度，取值介于 0.0（透明）和 1.0（不透明）之间。此属性与属性相反[getTransparency()](../../com.aspose.words/fill\#getTransparency--) / [setTransparency(double)](../../com.aspose.words/fill\#setTransparency-double-).

**退货:**
double - 指定填充的不透明度程度，值介于 0.0（透明）和 1.0（不透明）之间。
### getPattern() {#getPattern--}
```
public int getPattern()
```


得到一个[Pattern类型](../../com.aspose.words/patterntype)为填充。

**退货:**
诠释 - A[Pattern类型](../../com.aspose.words/patterntype)为填充。返回值是以下之一[Pattern类型](../../com.aspose.words/patterntype)常数。
### getPresetTexture() {#getPresetTexture--}
```
public int getPresetTexture()
```


得到一个[PresetTexture](../../com.aspose.words/presettexture)为填充。

**退货:**
诠释 - A[PresetTexture](../../com.aspose.words/presettexture)为填充。返回值是以下之一[PresetTexture](../../com.aspose.words/presettexture)常数。
### getRotateWithObject() {#getRotateWithObject--}
```
public boolean getRotateWithObject()
```


获取填充是否随指定对象旋转。

**退货:**
boolean - 填充是否随指定对象旋转。
### getTextureAlignment() {#getTextureAlignment--}
```
public int getTextureAlignment()
```


获取平铺纹理填充的对齐方式。

**退货:**
 int - 平铺纹理填充的对齐方式。返回值是以下之一[TextureAlignment](../../com.aspose.words/texturealignment)常数。
### getTransparency() {#getTransparency--}
```
public double getTransparency()
```


获取指定填充的透明度，作为 0.0（不透明）和 1.0（透明）之间的值。此属性与属性相反[getOpacity()](../../com.aspose.words/fill\#getOpacity--) / [setOpacity(double)](../../com.aspose.words/fill\#setOpacity-double-).

**退货:**
double - 指定填充的透明度，值介于 0.0（不透明）和 1.0（透明）之间。
### getVisible() {#getVisible--}
```
public boolean getVisible()
```


如果应用于此实例的格式可见，则获取值为 true。

**退货:**
boolean - 如果应用于此实例的格式可见，则该值为 true。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### oneColorGradient(int style, int variant, double degree) {#oneColorGradient-int-int-double-}
```
public void oneColorGradient(int style, int variant, double degree)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| style | int |  |
| variant | int |  |
| degree | double |  |

### oneColorGradient(Color color, int style, int variant, double degree) {#oneColorGradient-java.awt.Color-int-int-double-}
```
public void oneColorGradient(Color color, int style, int variant, double degree)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| color | java.awt.Color |  |
| style | int |  |
| variant | int |  |
| degree | double |  |

### patterned(int pattern类型) {#patterned-int-}
```
public void patterned(int pattern类型)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pattern类型 | int |  |

### patterned(int pattern类型, Color foreColor, Color backColor) {#patterned-int-java.awt.Color-java.awt.Color-}
```
public void patterned(int pattern类型, Color foreColor, Color backColor)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pattern类型 | int |  |
| foreColor | java.awt.Color |  |
| backColor | java.awt.Color |  |

### presetTextured(int presetTexture) {#presetTextured-int-}
```
public void presetTextured(int presetTexture)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| presetTexture | int |  |

### setBackColor(Color value) {#setBackColor-java.awt.Color-}
```
public void setBackColor(Color value)
```


设置表示填充背景颜色的 Color 对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color | 一个 Color 对象，表示填充的背景颜色。 |

### setColor(Color value) {#setColor-java.awt.Color-}
```
public void setColor(Color value)
```


设置表示填充的前景色的 Color 对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color | 一个 Color 对象，表示填充的前景色。 |

### setForeColor(Color value) {#setForeColor-java.awt.Color-}
```
public void setForeColor(Color value)
```


设置表示填充的前景色的 Color 对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color | 一个 Color 对象，表示填充的前景色。 |

### setGradientAngle(double value) {#setGradientAngle-double-}
```
public void setGradientAngle(double value)
```


设置渐变填充的角度。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 渐变填充的角度。 |

### setImage(byte[] imageBytes) {#setImage-byte---}
```
public void setImage(byte[] imageBytes)
```


将填充类型更改为单个图像。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| imageBytes | byte[] | 图像字节数组。 |

### setImage(InputStream stream) {#setImage-java.io.InputStream-}
```
public void setImage(InputStream stream)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### setImage(String fileName) {#setImage-java.lang.String-}
```
public void setImage(String fileName)
```


将填充类型更改为单个图像。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 图像文件的路径。 |

### setOn(boolean value) {#setOn-boolean-}
```
public void setOn(boolean value)
```


如果应用于此实例的格式可见，则设置值为 true。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 如果应用于此实例的格式可见，则该值为 true。 |

### setOpacity(double value) {#setOpacity-double-}
```
public void setOpacity(double value)
```


将指定填充的不透明度设置为 0.0（透明）和 1.0（不透明）之间的值。此属性与属性相反[getTransparency()](../../com.aspose.words/fill\#getTransparency--) / [setTransparency(double)](../../com.aspose.words/fill\#setTransparency-double-).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 指定填充的不透明度，值介于 0.0（透明）和 1.0（不透明）之间。 |

### setRotateWithObject(boolean value) {#setRotateWithObject-boolean-}
```
public void setRotateWithObject(boolean value)
```


设置填充是否随指定对象旋转。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 填充是否随指定对象旋转。 |

### setTextureAlignment(int value) {#setTextureAlignment-int-}
```
public void setTextureAlignment(int value)
```


设置平铺纹理填充的对齐方式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 平铺纹理填充的对齐方式。该值必须是以下之一[TextureAlignment](../../com.aspose.words/texturealignment)常数。 |

### setTransparency(double value) {#setTransparency-double-}
```
public void setTransparency(double value)
```


将指定填充的透明度设置为 0.0（不透明）和 1.0（透明）之间的值。此属性与属性相反[getOpacity()](../../com.aspose.words/fill\#getOpacity--) / [setOpacity(double)](../../com.aspose.words/fill\#setOpacity-double-).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 指定填充的透明度，值介于 0.0（不透明）和 1.0（透明）之间。 |

### setVisible(boolean value) {#setVisible-boolean-}
```
public void setVisible(boolean value)
```


如果应用于此实例的格式可见，则设置值为 true。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 如果应用于此实例的格式可见，则该值为 true。 |

### solid() {#solid--}
```
public void solid()
```


将填充设置为统一颜色。使用此方法可将任何填充转换回实体填充。

### solid(Color color) {#solid-java.awt.Color-}
```
public void solid(Color color)
```


将填充设置为指定的统一颜色。使用此方法可将任何填充转换回实体填充。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| color | java.awt.Color |  |

### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### twoColorGradient(int style, int variant) {#twoColorGradient-int-int-}
```
public void twoColorGradient(int style, int variant)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| style | int |  |
| variant | int |  |

### twoColorGradient(Color color1, Color color2, int style, int variant) {#twoColorGradient-java.awt.Color-java.awt.Color-int-int-}
```
public void twoColorGradient(Color color1, Color color2, int style, int variant)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| color1 | java.awt.Color |  |
| color2 | java.awt.Color |  |
| style | int |  |
| variant | int |  |

### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
