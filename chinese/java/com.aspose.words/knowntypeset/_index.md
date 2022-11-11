---
title: Known类型Set
second_title: Aspose.Words for Java API 参考
description:表示一个无序集，即
type: docs
weight: 356
url: /zh/java/com.aspose.words/knowntypeset/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
java.lang.Iterable
```
public class Known类型Set implements Iterable
```

表示包含 java.lang.班级 对象的无序集（即唯一项的集合），这些对象的完全或部分限定名称可在报告模板中用于调用相应类型的静态成员、执行类型转换等。

要了解更多信息，请访问**LINQ Reporting Engine**文档文章。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [add(班级 type)](#add-java.lang.班级-) | 将指定的 java.lang.班级 对象添加到集合中。 |
| [clear()](#clear--) | 从集合中移除所有项目。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getCount()](#getCount--) | 获取集合中项目的计数。 |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | 返回 一个 java.util.Iterator 对象，用于迭代集合中的项目。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(班级 type)](#remove-java.lang.班级-) | 从集合中移除指定的 java.lang.班级 对象。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(班级 type) {#add-java.lang.班级-}
```
public void add(班级 type)
```


将指定的 java.lang.班级 对象添加到集合中。在以下情况下抛出 java.lang.IllegalArgumentException：

\- 类型为空。

\- type 表示空类型。

\- type 表示不可见类型，即非公共类型或具有非公共外部类型的公共嵌套类型。

\- type 表示数组类型。

\- 类型已添加到集合中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| type | java.lang.班级 | 要添加的 java.lang.班级 对象。 |

### clear() {#clear--}
```
public void clear()
```


从集合中移除所有项目。

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
### getCount() {#getCount--}
```
public int getCount()
```


获取集合中项目的计数。

**退货:**
int - 集合中的项目数。
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


返回 一个 java.util.Iterator 对象，用于迭代集合中的项目。

**退货:**
java.util.Iterator - 一个 java.util.Iterator 对象，用于迭代集合中的项目。
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### remove(班级 type) {#remove-java.lang.班级-}
```
public void remove(班级 type)
```


从集合中移除指定的 java.lang.班级 对象。如果 type 为 null，则抛出 java.lang.IllegalArgumentException。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| type | java.lang.班级 | 要删除的 java.lang.班级 对象。 |

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
