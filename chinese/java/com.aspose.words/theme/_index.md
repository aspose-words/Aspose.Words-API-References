---
title: Theme
second_title: Aspose.Words for Java API 参考
description: 表示文档主题并提供对主要主题部分的访问，包括和
type: docs
weight: 573
url: /zh/java/com.aspose.words/theme/
---

**遗产：**
java.lang.Object

**所有已实现的接口：**
java.lang.Cloneable
```
public class Theme implements Cloneable
```

代表文档主题，并提供对主要主题部分的访问，包括[getMajorFonts()](../../com.aspose.words/theme\#getMajorFonts--), [getMinorFonts()](../../com.aspose.words/theme\#getMinorFonts--)和[getColors()](../../com.aspose.words/theme\#getColors--)

要了解更多信息，请访问**Working with Styles and Themes**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getColors()](#getColors--) | 允许为文档指定一组主题颜色。 |
| [getFontName(int themeFont)](#getFontName-int-) |  |
| [getMajorFonts()](#getMajorFonts--) | 允许为不同语言指定一组主要字体。 |
| [getMinorFonts()](#getMinorFonts--) | 允许为不同语言指定一组次要字体。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [onChange()](#onChange--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货：**
布尔值
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getColors() {#getColors--}
```
public ThemeColors getColors()
```


允许为文档指定一组主题颜色。

**退货：**
[ThemeColors](../../com.aspose.words/themecolors) - 相应的[ThemeColors](../../com.aspose.words/themecolors)价值。
### getFontName(int themeFont) {#getFontName-int-}
```
public String getFontName(int themeFont)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| themeFont | int |  |

**退货：**
java.lang.字符串
### getMajorFonts() {#getMajorFonts--}
```
public ThemeFonts getMajorFonts()
```


允许为不同语言指定一组主要字体。

**退货：**
[ThemeFonts](../../com.aspose.words/themefonts) - 相应的[ThemeFonts](../../com.aspose.words/themefonts)价值。
### getMinorFonts() {#getMinorFonts--}
```
public ThemeFonts getMinorFonts()
```


允许为不同语言指定一组次要字体。

**退货：**
[ThemeFonts](../../com.aspose.words/themefonts) - 相应的[ThemeFonts](../../com.aspose.words/themefonts)价值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### onChange() {#onChange--}
```
public void onChange()
```




### toString() {#toString--}
```
public String toString()
```




**退货：**
java.lang.字符串
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
