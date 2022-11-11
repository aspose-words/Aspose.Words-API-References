---
title: TextPath
second_title: Aspose.Words for Java API Reference
description: 定义艺术字对象的文本路径的文本和格式。
type: docs
weight: 567
url: /zh/java/com.aspose.words/textpath/
---

**遗产:**
java.lang.Object
```
public class TextPath
```

定义文本路径（艺术字对象）的文本和格式。

要了解更多信息，请访问**Working with Shapes**文档文章。

使用[Shape.getTextPath()](../../com.aspose.words/shape\#getTextPath--)属性以访问形状的艺术字属性。您不创建的实例[TextPath](../../com.aspose.words/textpath)直接上课。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBold()](#getBold--) | 如果字体格式为粗体，则为真。 |
| [get班级()](#get班级--) |  |
| [getFitPath()](#getFitPath--) | 定义文本是否适合形状的路径。 |
| [getFitShape()](#getFitShape--) | 定义文本是否适合形状的边界框。 |
| [getFontFamily()](#getFontFamily--) | 定义 textpath 字体的系列。 |
| [getItalic()](#getItalic--) | 如果字体格式为斜体，则为真。 |
| [getKerning()](#getKerning--) | 确定是否打开字距调整。 |
| [getOn()](#getOn--) | 定义是否显示文本。 |
| [getReverseRows()](#getReverseRows--) | 确定行的布局顺序是否颠倒。 |
| [getRotateLetters()](#getRotateLetters--) | 确定是否旋转文本的字母。 |
| [getSameLetterHeights()](#getSameLetterHeights--) | 确定无论初始大小写如何，所有字母是否都将具有相同的高度。 |
| [getShadow()](#getShadow--) | 定义是否对文本路径上的文本应用阴影。 |
| [getSize()](#getSize--) | 以磅为单位定义字体的大小。 |
| [getSmallCaps()](#getSmallCaps--) | 如果字体格式为小写大写字母，则为真。 |
| [getSpacing()](#getSpacing--) | 定义文本的间距量。 |
| [getStrikeThrough()](#getStrikeThrough--) | 如果字体格式设置为删除线文本，则为真。 |
| [getText()](#getText--) | 定义文本路径的文本。 |
| [getTextPathAlignment()](#getTextPathAlignment--) | 定义文本的对齐方式。 |
| [getTrim()](#getTrim--) | 确定是否删除文本上方和下方的多余空格。 |
| [getUnderline()](#getUnderline--) | 如果字体有下划线，则为真。 |
| [getXScale()](#getXScale--) | 确定是否将使用直文本路径而不是形状路径。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setBold(boolean value)](#setBold-boolean-) | 如果字体格式为粗体，则为真。 |
| [setFitPath(boolean value)](#setFitPath-boolean-) | 定义文本是否适合形状的路径。 |
| [setFitShape(boolean value)](#setFitShape-boolean-) | 定义文本是否适合形状的边界框。 |
| [setFontFamily(String value)](#setFontFamily-java.lang.String-) | 定义 textpath 字体的系列。 |
| [setItalic(boolean value)](#setItalic-boolean-) | 如果字体格式为斜体，则为真。 |
| [setKerning(boolean value)](#setKerning-boolean-) | 确定是否打开字距调整。 |
| [setOn(boolean value)](#setOn-boolean-) | 定义是否显示文本。 |
| [setReverseRows(boolean value)](#setReverseRows-boolean-) | 确定行的布局顺序是否颠倒。 |
| [setRotateLetters(boolean value)](#setRotateLetters-boolean-) | 确定是否旋转文本的字母。 |
| [setSameLetterHeights(boolean value)](#setSameLetterHeights-boolean-) | 确定无论初始大小写如何，所有字母是否都将具有相同的高度。 |
| [setShadow(boolean value)](#setShadow-boolean-) | 定义是否对文本路径上的文本应用阴影。 |
| [setSize(double value)](#setSize-double-) | 以磅为单位定义字体的大小。 |
| [setSmallCaps(boolean value)](#setSmallCaps-boolean-) | 如果字体格式为小写大写字母，则为真。 |
| [setSpacing(double value)](#setSpacing-double-) | 定义文本的间距量。 |
| [setStrikeThrough(boolean value)](#setStrikeThrough-boolean-) | 如果字体格式设置为删除线文本，则为真。 |
| [setText(String value)](#setText-java.lang.String-) | 定义文本路径的文本。 |
| [setTextPathAlignment(int value)](#setTextPathAlignment-int-) | 定义文本的对齐方式。 |
| [setTrim(boolean value)](#setTrim-boolean-) | 确定是否删除文本上方和下方的多余空格。 |
| [setUnderline(boolean value)](#setUnderline-boolean-) | 如果字体有下划线，则为真。 |
| [setXScale(boolean value)](#setXScale-boolean-) | 确定是否将使用直文本路径而不是形状路径。 |
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
### getBold() {#getBold--}
```
public boolean getBold()
```


如果字体格式为粗体，则为真。

默认值为**false**.

**退货:**
boolean - 对应的布尔值。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getFitPath() {#getFitPath--}
```
public boolean getFitPath()
```


定义文本是否适合形状的路径。

默认值为**false**.

**退货:**
boolean - 对应的布尔值。
### getFitShape() {#getFitShape--}
```
public boolean getFitShape()
```


定义文本是否适合形状的边界框。

默认值为**false**.

**退货:**
boolean - 对应的布尔值。
### getFontFamily() {#getFontFamily--}
```
public String getFontFamily()
```


定义 textpath 字体的系列。

默认值为 Arial。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getItalic() {#getItalic--}
```
public boolean getItalic()
```


如果字体格式为斜体，则为真。

默认值为**false**.

**退货:**
boolean - 对应的布尔值。
### getKerning() {#getKerning--}
```
public boolean getKerning()
```


确定是否打开字距调整。

默认值为**false**.

**退货:**
boolean - 对应的布尔值。
### getOn() {#getOn--}
```
public boolean getOn()
```


定义是否显示文本。

默认值为**false**.

**退货:**
boolean - 对应的布尔值。
### getReverseRows() {#getReverseRows--}
```
public boolean getReverseRows()
```


确定行的布局顺序是否颠倒。

默认值为**false**.

如果**true**，行的布局顺序是相反的。此属性用于垂直文本布局。

**退货:**
boolean - 对应的布尔值。
### getRotateLetters() {#getRotateLetters--}
```
public boolean getRotateLetters()
```


确定是否旋转文本的字母。

默认值为**false**.

**退货:**
boolean - 对应的布尔值。
### getSameLetterHeights() {#getSameLetterHeights--}
```
public boolean getSameLetterHeights()
```


确定无论初始大小写如何，所有字母是否都将具有相同的高度。

默认值为**false**.

**退货:**
boolean - 对应的布尔值。
### getShadow() {#getShadow--}
```
public boolean getShadow()
```


定义是否对文本路径上的文本应用阴影。

默认值为**false**.

**退货:**
boolean - 对应的布尔值。
### getSize() {#getSize--}
```
public double getSize()
```


以磅为单位定义字体的大小。

默认值为 36。

**退货:**
double - 对应的双精度值。
### getSmallCaps() {#getSmallCaps--}
```
public boolean getSmallCaps()
```


如果字体格式为小写大写字母，则为真。

默认值为**false**.

**退货:**
boolean - 对应的布尔值。
### getSpacing() {#getSpacing--}
```
public double getSpacing()
```


定义文本的间距量。 1 表示 100%。

默认值为 1。

**退货:**
double - 对应的双精度值。
### getStrikeThrough() {#getStrikeThrough--}
```
public boolean getStrikeThrough()
```


如果字体格式设置为删除线文本，则为真。

默认值为**false**.

**退货:**
boolean - 对应的布尔值。
### getText() {#getText--}
```
public String getText()
```


定义文本路径的文本。

默认值为空字符串。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getTextPathAlignment() {#getTextPathAlignment--}
```
public int getTextPathAlignment()
```


定义文本的对齐方式。

默认值为[TextPathAlignment.CENTER](../../com.aspose.words/textpathalignment\#CENTER).

**退货:**
int - 对应的 int 值。返回值是以下之一[TextPathAlignment](../../com.aspose.words/textpathalignment)常数。
### getTrim() {#getTrim--}
```
public boolean getTrim()
```


确定是否删除文本上方和下方的多余空格。

默认值为**false**.

**退货:**
boolean - 对应的布尔值。
### getUnderline() {#getUnderline--}
```
public boolean getUnderline()
```


如果字体有下划线，则为真。

默认值为**false**.

**退货:**
boolean - 对应的布尔值。
### getXScale() {#getXScale--}
```
public boolean getXScale()
```


确定是否将使用直文本路径而不是形状路径。

默认值为**false**.

如果**true**，文本沿着形状下边界的 x 值从左到右运行。

**退货:**
boolean - 对应的布尔值。
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




### setBold(boolean value) {#setBold-boolean-}
```
public void setBold(boolean value)
```


如果字体格式为粗体，则为真。

默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setFitPath(boolean value) {#setFitPath-boolean-}
```
public void setFitPath(boolean value)
```


定义文本是否适合形状的路径。

默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setFitShape(boolean value) {#setFitShape-boolean-}
```
public void setFitShape(boolean value)
```


定义文本是否适合形状的边界框。

默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setFontFamily(String value) {#setFontFamily-java.lang.String-}
```
public void setFontFamily(String value)
```


定义 textpath 字体的系列。

默认值为 Arial。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setItalic(boolean value) {#setItalic-boolean-}
```
public void setItalic(boolean value)
```


如果字体格式为斜体，则为真。

默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setKerning(boolean value) {#setKerning-boolean-}
```
public void setKerning(boolean value)
```


确定是否打开字距调整。

默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setOn(boolean value) {#setOn-boolean-}
```
public void setOn(boolean value)
```


定义是否显示文本。

默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setReverseRows(boolean value) {#setReverseRows-boolean-}
```
public void setReverseRows(boolean value)
```


确定行的布局顺序是否颠倒。

默认值为**false**.

如果**true**，行的布局顺序是相反的。此属性用于垂直文本布局。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setRotateLetters(boolean value) {#setRotateLetters-boolean-}
```
public void setRotateLetters(boolean value)
```


确定是否旋转文本的字母。

默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSameLetterHeights(boolean value) {#setSameLetterHeights-boolean-}
```
public void setSameLetterHeights(boolean value)
```


确定无论初始大小写如何，所有字母是否都将具有相同的高度。

默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setShadow(boolean value) {#setShadow-boolean-}
```
public void setShadow(boolean value)
```


定义是否对文本路径上的文本应用阴影。

默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSize(double value) {#setSize-double-}
```
public void setSize(double value)
```


以磅为单位定义字体的大小。

默认值为 36。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 对应的双精度值。 |

### setSmallCaps(boolean value) {#setSmallCaps-boolean-}
```
public void setSmallCaps(boolean value)
```


如果字体格式为小写大写字母，则为真。

默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSpacing(double value) {#setSpacing-double-}
```
public void setSpacing(double value)
```


定义文本的间距量。 1 表示 100%。

默认值为 1。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 对应的双精度值。 |

### setStrikeThrough(boolean value) {#setStrikeThrough-boolean-}
```
public void setStrikeThrough(boolean value)
```


如果字体格式设置为删除线文本，则为真。

默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setText(String value) {#setText-java.lang.String-}
```
public void setText(String value)
```


定义文本路径的文本。

默认值为空字符串。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setTextPathAlignment(int value) {#setTextPathAlignment-int-}
```
public void setTextPathAlignment(int value)
```


定义文本的对齐方式。

默认值为[TextPathAlignment.CENTER](../../com.aspose.words/textpathalignment\#CENTER).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[TextPathAlignment](../../com.aspose.words/textpathalignment)常数。 |

### setTrim(boolean value) {#setTrim-boolean-}
```
public void setTrim(boolean value)
```


确定是否删除文本上方和下方的多余空格。

默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setUnderline(boolean value) {#setUnderline-boolean-}
```
public void setUnderline(boolean value)
```


如果字体有下划线，则为真。

默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setXScale(boolean value) {#setXScale-boolean-}
```
public void setXScale(boolean value)
```


确定是否将使用直文本路径而不是形状路径。

默认值为**false**.

如果**true**，文本沿着形状下边界的 x 值从左到右运行。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

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
