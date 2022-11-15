---
title: HyphenationOptions
second_title: Aspose.Words for Java API 参考
description: 允许配置文档断字选项。
type: docs
weight: 334
url: /zh/java/com.aspose.words/hyphenationoptions/
---

**遗产：**
java.lang.Object

**所有已实现的接口：**
java.lang.Cloneable
```
public class HyphenationOptions implements Cloneable
```

允许配置文档断字选项。

要了解更多信息，请访问**Working with Hyphenation**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAutoHyphenation()](#getAutoHyphenation--) | 获取确定是否为文档打开自动断字的值。 |
| [getClass()](#getClass--) |  |
| [getConsecutiveHyphenLimit()](#getConsecutiveHyphenLimit--) | 获取可以以连字符结尾的最大连续行数。 |
| [getHyphenateCaps()](#getHyphenateCaps--) | 获取确定以大写字母书写的单词是否带有连字符的值。 |
| [getHyphenationZone()](#getHyphenationZone--) | 获取距您不想连字的单词的右边距的 1/20 点的距离。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAutoHyphenation(boolean value)](#setAutoHyphenation-boolean-) | 设置确定是否为文档打开自动断字的值。 |
| [setConsecutiveHyphenLimit(int value)](#setConsecutiveHyphenLimit-int-) | 设置可以以连字符结尾的最大连续行数。 |
| [setHyphenateCaps(boolean value)](#setHyphenateCaps-boolean-) | 设置值以确定是否用所有大写字母书写的单词都用连字符连接。 |
| [setHyphenationZone(int value)](#setHyphenationZone-int-) | 设置距右边距一个点的 1/20 的距离，您不想在该距离内对单词进行断字。 |
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
### getAutoHyphenation() {#getAutoHyphenation--}
```
public boolean getAutoHyphenation()
```


获取确定是否为文档打开自动断字的值。此属性的默认值为**false**.

**退货：**
boolean - 确定是否为文档打开自动断字的值。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getConsecutiveHyphenLimit() {#getConsecutiveHyphenLimit--}
```
public int getConsecutiveHyphenLimit()
```


获取可以以连字符结尾的最大连续行数。此属性的默认值为 0。

如果此属性的值设置为 0，则任意数量的连续行都可以以连字符结尾。

保存为固定页面格式（例如 PDF）时，该属性无效。

**退货：**
int - 可以以连字符结尾的最大连续行数。
### getHyphenateCaps() {#getHyphenateCaps--}
```
public boolean getHyphenateCaps()
```


获取确定以大写字母书写的单词是否带有连字符的值。此属性的默认值为**true**.

**退货：**
boolean - 确定以大写字母书写的单词是否带有连字符的值。
### getHyphenationZone() {#getHyphenationZone--}
```
public int getHyphenationZone()
```


获取距您不想连字的单词的右边距的 1/20 点的距离。此属性的默认值为 360（0.25 英寸）。

**退货：**
int - 距右边距的 1/20 点的距离，在该距离内您不想连字。
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




### setAutoHyphenation(boolean value) {#setAutoHyphenation-boolean-}
```
public void setAutoHyphenation(boolean value)
```


设置确定是否为文档打开自动断字的值。此属性的默认值为**false**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 确定是否为文档打开自动断字的值。 |

### setConsecutiveHyphenLimit(int value) {#setConsecutiveHyphenLimit-int-}
```
public void setConsecutiveHyphenLimit(int value)
```


设置可以以连字符结尾的最大连续行数。此属性的默认值为 0。

如果此属性的值设置为 0，则任意数量的连续行都可以以连字符结尾。

保存为固定页面格式（例如 PDF）时，该属性无效。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 可以以连字符结尾的最大连续行数。 |

### setHyphenateCaps(boolean value) {#setHyphenateCaps-boolean-}
```
public void setHyphenateCaps(boolean value)
```


设置值以确定是否用所有大写字母书写的单词都用连字符连接。此属性的默认值为**true**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 确定以所有大写字母书写的单词是否用连字符连接的值。 |

### setHyphenationZone(int value) {#setHyphenationZone-int-}
```
public void setHyphenationZone(int value)
```


设置距右边距一个点的 1/20 的距离，您不想在该距离内对单词进行断字。此属性的默认值为 360（0.25 英寸）。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 距右边距 1/20 点的距离，您不想在该距离内对单词进行断字。 |

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
