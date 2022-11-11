---
title: EndnoteOptions
second_title: Aspose.Words for Java API 参考
description: 表示文档或部分的尾注编号选项。
type: docs
weight: 146
url: /zh/java/com.aspose.words/endnoteoptions/
---

**遗产:**
java.lang.Object
```
public class EndnoteOptions
```

表示文档或部分的尾注编号选项。

要了解更多信息，请访问**Working with Footnote and Endnote**文档文章。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getLocation()](#getLocation--) |  |
| [getNumberStyle()](#getNumberStyle--) | 指定自动编号尾注的编号格式。 |
| [getPosition()](#getPosition--) | 指定尾注位置。 |
| [getRestartRule()](#getRestartRule--) | 确定自动编号何时重新开始。 |
| [getStartNumber()](#getStartNumber--) | 指定第一个自动编号的尾注的起始编号或字符。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setLocation(int value)](#setLocation-int-) |  |
| [setNumberStyle(int value)](#setNumberStyle-int-) | 指定自动编号尾注的编号格式。 |
| [setPosition(int value)](#setPosition-int-) | 指定尾注位置。 |
| [setRestartRule(int value)](#setRestartRule-int-) | 确定自动编号何时重新开始。 |
| [setStartNumber(int value)](#setStartNumber-int-) | 指定第一个自动编号的尾注的起始编号或字符。 |
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
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getLocation() {#getLocation--}
```
public int getLocation()
```




**退货:**
整数
### getNumberStyle() {#getNumberStyle--}
```
public int getNumberStyle()
```


指定自动编号尾注的编号格式。

并非所有数字样式都适用于此属性。有关适用编号样式的列表，请参见 Microsoft Word 中的插入脚注或尾注对话框。如果您选择不适用的数字样式，Microsoft Word 将恢复为默认值。

**退货:**
int - 对应的 int 值。返回值是以下之一[NumberStyle](../../com.aspose.words/numberstyle)常数。
### getPosition() {#getPosition--}
```
public int getPosition()
```


指定尾注位置。

**退货:**
int - 对应的 int 值。返回值是以下之一[EndnotePosition](../../com.aspose.words/endnoteposition)常数。
### getRestartRule() {#getRestartRule--}
```
public int getRestartRule()
```


确定自动编号何时重新开始。

并非所有值都适用于尾注。要确定哪些值适用，请参阅[FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule).

**退货:**
int - 对应的 int 值。返回值是以下之一[FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule)常数。
### getStartNumber() {#getStartNumber--}
```
public int getStartNumber()
```


指定第一个自动编号的尾注的起始编号或字符。

此属性仅在以下情况下有效[getRestartRule()](../../com.aspose.words/endnoteoptions\#getRestartRule--) / [setRestartRule(int)](../../com.aspose.words/endnoteoptions\#setRestartRule-int-)被设定为[FootnoteNumberingRule.CONTINUOUS](../../com.aspose.words/footnotenumberingrule\#CONTINUOUS).

**退货:**
int - 对应的 int 值。
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




### setLocation(int value) {#setLocation-int-}
```
public void setLocation(int value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int |  |

### setNumberStyle(int value) {#setNumberStyle-int-}
```
public void setNumberStyle(int value)
```


指定自动编号尾注的编号格式。

并非所有数字样式都适用于此属性。有关适用编号样式的列表，请参见 Microsoft Word 中的插入脚注或尾注对话框。如果您选择不适用的数字样式，Microsoft Word 将恢复为默认值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[NumberStyle](../../com.aspose.words/numberstyle)常数。 |

### setPosition(int value) {#setPosition-int-}
```
public void setPosition(int value)
```


指定尾注位置。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[EndnotePosition](../../com.aspose.words/endnoteposition)常数。 |

### setRestartRule(int value) {#setRestartRule-int-}
```
public void setRestartRule(int value)
```


确定自动编号何时重新开始。

并非所有值都适用于尾注。要确定哪些值适用，请参阅[FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[FootnoteNumberingRule](../../com.aspose.words/footnotenumberingrule)常数。 |

### setStartNumber(int value) {#setStartNumber-int-}
```
public void setStartNumber(int value)
```


指定第一个自动编号的尾注的起始编号或字符。

此属性仅在以下情况下有效[getRestartRule()](../../com.aspose.words/endnoteoptions\#getRestartRule--) / [setRestartRule(int)](../../com.aspose.words/endnoteoptions\#setRestartRule-int-)被设定为[FootnoteNumberingRule.CONTINUOUS](../../com.aspose.words/footnotenumberingrule\#CONTINUOUS).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。 |

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
