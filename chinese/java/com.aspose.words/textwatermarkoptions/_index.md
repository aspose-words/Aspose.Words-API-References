---
title: TextWatermarkOptions
second_title: Aspose.Words for Java API 参考
description: 包含在添加带有文本的水印时可以指定的选项。
type: docs
weight: 569
url: /zh/java/com.aspose.words/textwatermarkoptions/
---

**遗产:**
java.lang.Object
```
public class TextWatermarkOptions
```

包含在添加带有文本的水印时可以指定的选项。

要了解更多信息，请访问**Working with Watermark**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getColor()](#getColor--) | 获取字体颜色。 |
| [getFontFamily()](#getFontFamily--) | 获取字体系列名称。 |
| [getFontSize()](#getFontSize--) | 获取字体大小。 |
| [getLayout()](#getLayout--) | 获取水印的布局。 |
| [hashCode()](#hashCode--) |  |
| [isSemitrasparent()](#isSemitrasparent--) | 获取一个布尔值，它负责水印的不透明度。 |
| [isSemitrasparent(boolean value)](#isSemitrasparent-boolean-) | 设置一个布尔值，它负责水印的不透明度。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setColor(Color value)](#setColor-java.awt.Color-) | 设置字体颜色。 |
| [setFontFamily(String value)](#setFontFamily-java.lang.String-) | 设置字体系列名称。 |
| [setFontSize(float value)](#setFontSize-float-) | 设置字体大小。 |
| [setLayout(int value)](#setLayout-int-) | 设置水印的布局。 |
| [toString()](#toString--) |  |
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getColor() {#getColor--}
```
public Color getColor()
```


获取字体颜色。默认值为 Color.Silver。

**退货:**
java.awt.Color - 字体颜色。
### getFontFamily() {#getFontFamily--}
```
public String getFontFamily()
```


获取字体系列名称。默认值为“Calibri”。

**退货:**
java.lang.String - 字体系列名称。
### getFontSize() {#getFontSize--}
```
public float getFontSize()
```


获取字体大小。默认值为 0 - 自动。

有效值范围从 0 到 65.5（含）。

自动字体大小意味着水印将缩放到其相对于页边距的最大宽度和最大高度。

**退货:**
float - 字体大小。
### getLayout() {#getLayout--}
```
public int getLayout()
```


获取水印的布局。默认值为[WatermarkLayout.DIAGONAL](../../com.aspose.words/watermarklayout\#DIAGONAL).

**退货:**
int - 水印的布局。返回值是以下之一[WatermarkLayout](../../com.aspose.words/watermarklayout)常数。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isSemitrasparent() {#isSemitrasparent--}
```
public boolean isSemitrasparent()
```


获取一个布尔值，它负责水印的不透明度。默认值是true。

**退货:**
boolean - 一个布尔值，负责水印的不透明度。
### isSemitrasparent(boolean value) {#isSemitrasparent-boolean-}
```
public void isSemitrasparent(boolean value)
```


设置一个布尔值，它负责水印的不透明度。默认值是true。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，负责水印的不透明度。 |

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setColor(Color value) {#setColor-java.awt.Color-}
```
public void setColor(Color value)
```


设置字体颜色。默认值为 Color.Silver。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color | 字体颜色。 |

### setFontFamily(String value) {#setFontFamily-java.lang.String-}
```
public void setFontFamily(String value)
```


设置字体系列名称。默认值为“Calibri”。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 字体系列名称。 |

### setFontSize(float value) {#setFontSize-float-}
```
public void setFontSize(float value)
```


设置字体大小。默认值为 0 - 自动。

有效值范围从 0 到 65.5（含）。

自动字体大小意味着水印将缩放到其相对于页边距的最大宽度和最大高度。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | float | 字体大小。 |

### setLayout(int value) {#setLayout-int-}
```
public void setLayout(int value)
```


设置水印的布局。默认值为[WatermarkLayout.DIAGONAL](../../com.aspose.words/watermarklayout\#DIAGONAL).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 水印的布局。该值必须是其中之一[WatermarkLayout](../../com.aspose.words/watermarklayout)常数。 |

### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
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
