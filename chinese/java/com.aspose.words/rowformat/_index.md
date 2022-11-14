---
title: RowFormat
second_title: Aspose.Words for Java API 参考
description: 表示表格行的所有格式。
type: docs
weight: 494
url: /zh/java/com.aspose.words/rowformat/
---

**遗产:**
java.lang.Object
```
public class RowFormat
```

表示表格行的所有格式。

要了解更多信息，请访问**Working with Tables**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [clearFormatting()](#clearFormatting--) | 重置为默认行格式。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int-) |  |
| [getAllowBreakAcrossPages()](#getAllowBreakAcrossPages--) | 如果允许表格行中的文本跨分页符拆分，则为真。 |
| [getBorders()](#getBorders--) | 获取行的默认单元格边框的集合。 |
| [getClass()](#getClass--) |  |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int-) |  |
| [getHeadingFormat()](#getHeadingFormat--) | 当表格跨越多个页面时，如果该行在每一页上重复作为表格标题，则为真。 |
| [getHeight()](#getHeight--) | 获取表格行的高度（以磅为单位）。 |
| [getHeightRule()](#getHeightRule--) | 获取确定表格行高的规则。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAllowBreakAcrossPages(boolean value)](#setAllowBreakAcrossPages-boolean-) | 如果允许表格行中的文本跨分页符拆分，则为真。 |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object-) |  |
| [setHeadingFormat(boolean value)](#setHeadingFormat-boolean-) | 当表格跨越多个页面时，如果该行在每一页上重复作为表格标题，则为真。 |
| [setHeight(double value)](#setHeight-double-) | 以磅为单位设置表格行的高度。 |
| [setHeightRule(int value)](#setHeightRule-int-) | 设置确定表格行高的规则。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearFormatting() {#clearFormatting--}
```
public void clearFormatting()
```


重置为默认行格式。

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
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int-}
```
public Object fetchInheritedBorderAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getAllowBreakAcrossPages() {#getAllowBreakAcrossPages--}
```
public boolean getAllowBreakAcrossPages()
```


如果允许表格行中的文本跨分页符拆分，则为真。

**退货:**
boolean - 对应的布尔值。
### getBorders() {#getBorders--}
```
public BorderCollection getBorders()
```


获取行的默认单元格边框的集合。

**退货:**
[BorderCollection](../../com.aspose.words/bordercollection) - 行的默认单元格边框集合。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int-}
```
public Object getDirectBorderAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getHeadingFormat() {#getHeadingFormat--}
```
public boolean getHeadingFormat()
```


当表格跨越多个页面时，如果该行在每一页上重复作为表格标题，则为真。

**退货:**
boolean - 对应的布尔值。
### getHeight() {#getHeight--}
```
public double getHeight()
```


获取表格行的高度（以磅为单位）。

**退货:**
double - 表格行的高度（以磅为单位）。
### getHeightRule() {#getHeightRule--}
```
public int getHeightRule()
```


获取确定表格行高的规则。

**退货:**
 int - 确定表格行高的规则。返回值是以下之一[HeightRule](../../com.aspose.words/heightrule)常数。
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




### setAllowBreakAcrossPages(boolean value) {#setAllowBreakAcrossPages-boolean-}
```
public void setAllowBreakAcrossPages(boolean value)
```


如果允许表格行中的文本跨分页符拆分，则为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object-}
```
public void setBorderAttr(int key, Object value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setHeadingFormat(boolean value) {#setHeadingFormat-boolean-}
```
public void setHeadingFormat(boolean value)
```


当表格跨越多个页面时，如果该行在每一页上重复作为表格标题，则为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setHeight(double value) {#setHeight-double-}
```
public void setHeight(double value)
```


以磅为单位设置表格行的高度。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 表格行的高度（以磅为单位）。 |

### setHeightRule(int value) {#setHeightRule-int-}
```
public void setHeightRule(int value)
```


设置确定表格行高的规则。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 确定表格行高的规则。该值必须是其中之一[HeightRule](../../com.aspose.words/heightrule)常数。 |

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
