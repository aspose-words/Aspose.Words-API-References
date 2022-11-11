---
title: TextBox
second_title: Aspose.Words for Java API 参考
description:定义指定文本如何在形状内显示的属性。
type: docs
weight: 558
url: /zh/java/com.aspose.words/textbox/
---

**遗产:**
java.lang.Object
```
public class TextBox
```

定义指定文本如何在形状内显示的属性。

要了解更多信息，请访问**Working with Shapes**文档文章。

使用[Shape.getTextBox()](../../com.aspose.words/shape\#getTextBox--)属性来访问形状的文本属性。您不创建的实例[TextBox](../../com.aspose.words/textbox)直接上课。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [breakForwardLink()](#breakForwardLink--) | 断开到下一个文本框的链接。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getFitShapeToText()](#getFitShapeToText--) | 确定 Microsoft Word 是否会增大形状以适合文本。 |
| [getInternalMarginBottom()](#getInternalMarginBottom--) | 以磅为单位指定形状的内底边距。 |
| [getInternalMarginLeft()](#getInternalMarginLeft--) | 以磅为单位指定形状的内部左边距。 |
| [getInternalMarginRight()](#getInternalMarginRight--) | 以磅为单位指定形状的内部右边距。 |
| [getInternalMarginTop()](#getInternalMarginTop--) | 以磅为单位指定形状的内部上边距。 |
| [getLayoutFlow()](#getLayoutFlow--) | 确定形状中文本布局的流向。 |
| [getNext()](#getNext--) | 获取一个 TextBox，它表示形状序列中的下一个 TextBox。 |
| [getParent()](#getParent--) | 获取 TextBox 的父形状。 |
| [getPrevious()](#getPrevious--) | 返回一个 TextBox，它表示形状序列中的前一个 TextBox。 |
| [getTextBoxWrapMode()](#getTextBoxWrapMode--) | 确定文本在形状内的换行方式。 |
| [getVerticalAnchor()](#getVerticalAnchor--) | 指定形状内文本的垂直对齐方式。 |
| [hashCode()](#hashCode--) |  |
| [isValidLinkTarget(TextBox target)](#isValidLinkTarget-com.aspose.words.TextBox-) | 确定此 TextBox 是否可以链接到目标 Textbox。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setFitShapeToText(boolean value)](#setFitShapeToText-boolean-) | 确定 Microsoft Word 是否会增大形状以适合文本。 |
| [setInternalMarginBottom(double value)](#setInternalMarginBottom-double-) | 以磅为单位指定形状的内底边距。 |
| [setInternalMarginLeft(double value)](#setInternalMarginLeft-double-) | 以磅为单位指定形状的内部左边距。 |
| [setInternalMarginRight(double value)](#setInternalMarginRight-double-) | 以磅为单位指定形状的内部右边距。 |
| [setInternalMarginTop(double value)](#setInternalMarginTop-double-) | 以磅为单位指定形状的内部上边距。 |
| [setLayoutFlow(int value)](#setLayoutFlow-int-) | 确定形状中文本布局的流向。 |
| [setNext(TextBox value)](#setNext-com.aspose.words.TextBox-) | 设置一个表示形状序列中下一个 TextBox 的 TextBox。 |
| [setTextBoxWrapMode(int value)](#setTextBoxWrapMode-int-) | 确定文本在形状内的换行方式。 |
| [setVerticalAnchor(int value)](#setVerticalAnchor-int-) | 指定形状内文本的垂直对齐方式。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### breakForwardLink() {#breakForwardLink--}
```
public void breakForwardLink()
```


断开到下一个文本框的链接。 BreakForwardLink() 不会破坏当前形状序列中的所有其他链接。例如：1-2-3-4 序列和第二个文本框的 BreakForwardLink 将创建两个序列 1-2、3-4。

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
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getFitShapeToText() {#getFitShapeToText--}
```
public boolean getFitShapeToText()
```


确定 Microsoft Word 是否会增大形状以适合文本。

默认值为**false**.

**退货:**
boolean - 对应的布尔值。
### getInternalMarginBottom() {#getInternalMarginBottom--}
```
public double getInternalMarginBottom()
```


以磅为单位指定形状的内底边距。

默认值为 1/20 英寸。

**退货:**
double - 对应的双精度值。
### getInternalMarginLeft() {#getInternalMarginLeft--}
```
public double getInternalMarginLeft()
```


以磅为单位指定形状的内部左边距。

默认值为 1/10 英寸。

**退货:**
double - 对应的双精度值。
### getInternalMarginRight() {#getInternalMarginRight--}
```
public double getInternalMarginRight()
```


以磅为单位指定形状的内部右边距。

默认值为 1/10 英寸。

**退货:**
double - 对应的双精度值。
### getInternalMarginTop() {#getInternalMarginTop--}
```
public double getInternalMarginTop()
```


以磅为单位指定形状的内部上边距。

默认值为 1/20 英寸。

**退货:**
double - 对应的双精度值。
### getLayoutFlow() {#getLayoutFlow--}
```
public int getLayoutFlow()
```


确定形状中文本布局的流向。

默认值为[LayoutFlow.HORIZONTAL](../../com.aspose.words/layoutflow\#HORIZONTAL).

**退货:**
int - 对应的 int 值。返回值是以下之一[LayoutFlow](../../com.aspose.words/layoutflow)常数。
### getNext() {#getNext--}
```
public TextBox getNext()
```


获取一个 TextBox，它表示形状序列中的下一个 TextBox。

**退货:**
[TextBox](../../com.aspose.words/textbox) - 一个文本框，它代表一系列形状中的下一个文本框。
### getParent() {#getParent--}
```
public Shape getParent()
```


获取 TextBox 的父形状。

**退货:**
[Shape](../../com.aspose.words/shape) - 文本框的父形状。
### getPrevious() {#getPrevious--}
```
public TextBox getPrevious()
```


返回一个 TextBox，它表示形状序列中的前一个 TextBox。

**退货:**
[TextBox](../../com.aspose.words/textbox) - 一个文本框，它代表一系列形状中的前一个文本框。
### getTextBoxWrapMode() {#getTextBoxWrapMode--}
```
public int getTextBoxWrapMode()
```


确定文本在形状内的换行方式。

默认值为[TextBoxWrapMode.SQUARE](../../com.aspose.words/textboxwrapmode\#SQUARE).

**退货:**
int - 对应的 int 值。返回值是以下之一[TextBoxWrapMode](../../com.aspose.words/textboxwrapmode)常数。
### getVerticalAnchor() {#getVerticalAnchor--}
```
public int getVerticalAnchor()
```


指定形状内文本的垂直对齐方式。

默认值为[TextBoxAnchor.TOP](../../com.aspose.words/textboxanchor\#TOP).

**退货:**
int - 对应的 int 值。返回值是以下之一[TextBoxAnchor](../../com.aspose.words/textboxanchor)常数。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isValidLinkTarget(TextBox target) {#isValidLinkTarget-com.aspose.words.TextBox-}
```
public boolean isValidLinkTarget(TextBox target)
```


确定此 TextBox 是否可以链接到目标 Textbox。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| target | [TextBox](../../com.aspose.words/textbox) |  |

**退货:**
布尔值
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setFitShapeToText(boolean value) {#setFitShapeToText-boolean-}
```
public void setFitShapeToText(boolean value)
```


确定 Microsoft Word 是否会增大形状以适合文本。

默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setInternalMarginBottom(double value) {#setInternalMarginBottom-double-}
```
public void setInternalMarginBottom(double value)
```


以磅为单位指定形状的内底边距。

默认值为 1/20 英寸。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 对应的双精度值。 |

### setInternalMarginLeft(double value) {#setInternalMarginLeft-double-}
```
public void setInternalMarginLeft(double value)
```


以磅为单位指定形状的内部左边距。

默认值为 1/10 英寸。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 对应的双精度值。 |

### setInternalMarginRight(double value) {#setInternalMarginRight-double-}
```
public void setInternalMarginRight(double value)
```


以磅为单位指定形状的内部右边距。

默认值为 1/10 英寸。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 对应的双精度值。 |

### setInternalMarginTop(double value) {#setInternalMarginTop-double-}
```
public void setInternalMarginTop(double value)
```


以磅为单位指定形状的内部上边距。

默认值为 1/20 英寸。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 对应的双精度值。 |

### setLayoutFlow(int value) {#setLayoutFlow-int-}
```
public void setLayoutFlow(int value)
```


确定形状中文本布局的流向。

默认值为[LayoutFlow.HORIZONTAL](../../com.aspose.words/layoutflow\#HORIZONTAL).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[LayoutFlow](../../com.aspose.words/layoutflow)常数。 |

### setNext(TextBox value) {#setNext-com.aspose.words.TextBox-}
```
public void setNext(TextBox value)
```


设置一个表示形状序列中下一个 TextBox 的 TextBox。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [TextBox](../../com.aspose.words/textbox) | 表示形状序列中的下一个 TextBox 的 TextBox。 |

### setTextBoxWrapMode(int value) {#setTextBoxWrapMode-int-}
```
public void setTextBoxWrapMode(int value)
```


确定文本在形状内的换行方式。

默认值为[TextBoxWrapMode.SQUARE](../../com.aspose.words/textboxwrapmode\#SQUARE).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[TextBoxWrapMode](../../com.aspose.words/textboxwrapmode)常数。 |

### setVerticalAnchor(int value) {#setVerticalAnchor-int-}
```
public void setVerticalAnchor(int value)
```


指定形状内文本的垂直对齐方式。

默认值为[TextBoxAnchor.TOP](../../com.aspose.words/textboxanchor\#TOP).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[TextBoxAnchor](../../com.aspose.words/textboxanchor)常数。 |

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
