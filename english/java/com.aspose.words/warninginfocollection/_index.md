---
title: WarningInfoCollection
second_title: Aspose.Words for Java API Reference
description: 表示对象的类型化集合。
type: docs
weight: 605
url: /zh/java/com.aspose.words/warninginfocollection/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
[com.aspose.words.IWarningCallback](../../com.aspose.words/iwarningcallback), java.lang.Iterable
```
public class WarningInfoCollection implements IWarningCallback, Iterable
```

表示一个类型化的集合[WarningInfo](../../com.aspose.words/warninginfo)对象。

要了解更多信息，请访问**Programming with Documents**文档文章。

您可以将此集合对象用作最简单的形式[IWarningCallback](../../com.aspose.words/iwarningcallback)实现来收集 Aspose.Words 在加载或保存操作期间生成的所有警告。创建此类的一个实例并将其分配给[LoadOptions.getWarningCallback()](../../com.aspose.words/loadoptions\#getWarningCallback--) / [LoadOptions.setWarningCallback(com.aspose.words.IWarningCallback)](../../com.aspose.words/loadoptions\#setWarningCallback-com.aspose.words.IWarningCallback-)或者[DocumentBase.getWarningCallback()](../../com.aspose.words/documentbase\#getWarningCallback--) / [DocumentBase.setWarningCallback(com.aspose.words.IWarningCallback)](../../com.aspose.words/documentbase\#setWarningCallback-com.aspose.words.IWarningCallback-)财产。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [clear()](#clear--) | 从集合中移除所有元素。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 获取指定索引处的项目。 |
| [get班级()](#get班级--) |  |
| [getCount()](#getCount--) | 获取集合中包含的元素数。 |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | 返回一个迭代器对象，该对象可用于迭代集合中的所有项目。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
| [warning(WarningInfo info)](#warning-com.aspose.words.WarningInfo-) | 实施[IWarningCallback](../../com.aspose.words/iwarningcallback)界面。 |
### clear() {#clear--}
```
public void clear()
```


从集合中移除所有元素。

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
### get(int index) {#get-int-}
```
public WarningInfo get(int index)
```


获取指定索引处的项目。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 项目的从零开始的索引。 |

**退货:**
[WarningInfo](../../com.aspose.words/warninginfo) - 指定索引处的项目。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getCount() {#getCount--}
```
public int getCount()
```


获取集合中包含的元素数。

**退货:**
int - 集合中包含的元素数。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### iterator() {#iterator--}
```
public Iterator iterator()
```


返回一个迭代器对象，该对象可用于迭代集合中的所有项目。

**退货:**
java.util.Iterator
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




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

### warning(WarningInfo info) {#warning-com.aspose.words.WarningInfo-}
```
public void warning(WarningInfo info)
```


实施[IWarningCallback](../../com.aspose.words/iwarningcallback)界面。向此集合添加警告。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| info | [WarningInfo](../../com.aspose.words/warninginfo) |  |
