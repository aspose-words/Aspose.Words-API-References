---
title: TabStopCollection
second_title: Aspose.Words for Java API 参考
description: 代表段落或样式的自定义选项卡的对象集合。
type: docs
weight: 547
url: /zh/java/com.aspose.words/tabstopcollection/
---

**遗产：**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr)

**所有已实现的接口：**
java.lang.Cloneable
```
public class TabStopCollection extends InternableComplexAttr implements Cloneable
```

的集合[TabStop](../../com.aspose.words/tabstop)表示段落或样式的自定义选项卡的对象。

要了解更多信息，请访问**Aspose.Words Document Object Model (DOM)**文档文章。

在 Microsoft Word 文档中，可以在段落样式的属性中或直接在段落的属性中定义制表位。一种风格可以基于另一种风格。因此，给定对象的完整制表位集是直接在该对象上定义的制表位和从父样式继承的制表位的组合。

在 Aspose.Words 中，当您获得**TabStops**段落或样式的集合，它仅包含直接为此段落或样式定义的自定义制表位。该集合不包括在父样式或默认制表位中定义的制表位。
## 方法

| 方法 | 描述 |
| --- | --- |
| [add(TabStop tabStop)](#add-com.aspose.words.TabStop-) | 添加或替换集合中的制表位。 |
| [add(double position, int alignment, int leader)](#add-double-int-int-) |  |
| [after(double position)](#after-double-) | 获取指定位置右侧的第一个制表位。 |
| [before(double position)](#before-double-) | 获取指定位置左侧的第一个制表位。 |
| [clear()](#clear--) | 删除所有制表位位置。 |
| [equals(TabStopCollection rhs)](#equals-com.aspose.words.TabStopCollection-) | 确定指定的 TabStopCollection 的值是否等于当前的 TabStopCollection。 |
| [equals(Object obj)](#equals-java.lang.Object-) | 确定指定对象的值是否与当前对象相等。 |
| [get(double position)](#get-double-) | 获取指定位置的制表位。 |
| [get(int index)](#get-int-) | 从集合中检索制表位。 |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | 获取集合中制表位的数量。 |
| [getIndexByPosition(double position)](#getIndexByPosition-double-) | 获取具有指定位置（以磅为单位）的制表位索引。 |
| [getPositionByIndex(int index)](#getPositionByIndex-int-) | 获取指定索引处制表位的位置（以磅为单位）。 |
| [hashCode()](#hashCode--) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [removeByIndex(int index)](#removeByIndex-int-) | 从集合中删除指定索引处的制表位。 |
| [removeByPosition(double position)](#removeByPosition-double-) | 从集合中删除指定位置的制表位。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(TabStop tabStop) {#add-com.aspose.words.TabStop-}
```
public void add(TabStop tabStop)
```


添加或替换集合中的制表位。

如果指定位置已存在制表位，则将其替换。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| tabStop | [TabStop](../../com.aspose.words/tabstop) | 要添加的制表位对象。 |

### add(double position, int alignment, int leader) {#add-double-int-int-}
```
public void add(double position, int alignment, int leader)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| position | double |  |
| alignment | int |  |
| leader | int |  |

### after(double position) {#after-double-}
```
public TabStop after(double position)
```


获取指定位置右侧的第一个制表位。

跳过制表位**Alignment**设置为 TabAlignment.Bar 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| position | double | 参考位置（以点为单位）。 |

**退货：**
[TabStop](../../com.aspose.words/tabstop) - 如果未找到合适的制表位，则为制表位对象或 null。
### before(double position) {#before-double-}
```
public TabStop before(double position)
```


获取指定位置左侧的第一个制表位。

跳过制表位**Alignment**设置为 TabAlignment.Bar 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| position | double | 参考位置（以点为单位）。 |

**退货：**
[TabStop](../../com.aspose.words/tabstop) - 如果未找到合适的制表位，则为制表位对象或 null。
### clear() {#clear--}
```
public void clear()
```


删除所有制表位位置。

### equals(TabStopCollection rhs) {#equals-com.aspose.words.TabStopCollection-}
```
public boolean equals(TabStopCollection rhs)
```


确定指定的 TabStopCollection 的值是否等于当前的 TabStopCollection。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| rhs | [TabStopCollection](../../com.aspose.words/tabstopcollection) |  |

**退货：**
布尔值
### equals(Object obj) {#equals-java.lang.Object-}
```
public boolean equals(Object obj)
```


确定指定对象的值是否与当前对象相等。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| obj | java.lang.Object |  |

**退货：**
布尔值
### get(double position) {#get-double-}
```
public TabStop get(double position)
```


获取指定位置的制表位。如果在指定位置未找到制表位，则返回 null。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| position | double | 制表位的位置（以磅为单位）。 |

**退货：**
[TabStop](../../com.aspose.words/tabstop) - 指定位置的制表位。
### get(int index) {#get-int-}
```
public TabStop get(int index)
```


从集合中检索制表位。获取给定索引处的制表位。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 制表位集合的索引。 |

**退货：**
[TabStop](../../com.aspose.words/tabstop) - 相应的[TabStop](../../com.aspose.words/tabstop)价值。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getCount() {#getCount--}
```
public int getCount()
```


获取集合中制表位的数量。

**退货：**
int - 集合中制表位的数量。
### getIndexByPosition(double position) {#getIndexByPosition-double-}
```
public int getIndexByPosition(double position)
```


获取具有指定位置（以磅为单位）的制表位索引。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| position | double |  |

**退货：**
整数
### getPositionByIndex(int index) {#getPositionByIndex-int-}
```
public double getPositionByIndex(int index)
```


获取指定索引处制表位的位置（以磅为单位）。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 制表位集合的索引。 |

**退货：**
double - 制表位的位置。
### hashCode() {#hashCode--}
```
public int hashCode()
```




**退货：**
整数
### isInheritedComplexAttr() {#isInheritedComplexAttr--}
```
public boolean isInheritedComplexAttr()
```




**退货：**
布尔值
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### removeByIndex(int index) {#removeByIndex-int-}
```
public void removeByIndex(int index)
```


从集合中删除指定索引处的制表位。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 制表位集合的索引。 |

### removeByPosition(double position) {#removeByPosition-double-}
```
public void removeByPosition(double position)
```


从集合中删除指定位置的制表位。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| position | double | 要删除的制表位的位置（以磅为单位）。 |

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
