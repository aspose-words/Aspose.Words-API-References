---
title: ConstraintCollection
second_title: Aspose.Words for Java API 参考
description:表示 a 的一组约束。
type: docs
weight: 11
url: /zh/java/com.aspose.words.net.system.data/constraintcollection/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
java.lang.Iterable
```
public class ConstraintCollection implements Iterable
```

表示一个约束的集合[DataTable](../../com.aspose.words.net.system.data/datatable).
## 方法s

| 方法 | 描述 |
| --- | --- |
| [add(System.Data.Constraint constraint)](#add-com.aspose.words.net.System.Data.Constraint-) | 添加指定的[Constraint](../../com.aspose.words.net.system.data/constraint)反对集合。 |
| [contains(System.Data.Constraint cc)](#contains-com.aspose.words.net.System.Data.Constraint-) | 指示集合中是否存在 name 指定的 Constraint 对象。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 获取[Constraint](../../com.aspose.words.net.system.data/constraint)来自指定索引处的集合。 |
| [get(String name)](#get-java.lang.String-) | 获取[Constraint](../../com.aspose.words.net.system.data/constraint)从具有指定名称的集合中。 |
| [get班级()](#get班级--) |  |
| [getCount()](#getCount--) | 获取集合中元素的总数。 |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(System.Data.Constraint constraint)](#remove-com.aspose.words.net.System.Data.Constraint-) | 删除指定的[Constraint](../../com.aspose.words.net.system.data/constraint)从收藏。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(System.Data.Constraint constraint) {#add-com.aspose.words.net.System.Data.Constraint-}
```
public void add(System.Data.Constraint constraint)
```


添加指定的[Constraint](../../com.aspose.words.net.system.data/constraint)反对集合。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| constraint | [Constraint](../../com.aspose.words.net.system.data/constraint) | 要添加的约束。 |

### contains(System.Data.Constraint cc) {#contains-com.aspose.words.net.System.Data.Constraint-}
```
public boolean contains(System.Data.Constraint cc)
```


指示集合中是否存在 name 指定的 Constraint 对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| cc | [Constraint](../../com.aspose.words.net.system.data/constraint) | 要删除的约束。 |

**退货:**
boolean - 如果集合包含指定的约束，则为 true；否则为假。
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
public System.Data.Constraint get(int index)
```


获取[Constraint](../../com.aspose.words.net.system.data/constraint)来自指定索引处的集合。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 要返回的约束的索引。 |

**退货:**
[Constraint](../../com.aspose.words.net.system.data/constraint) - 这[Constraint](../../com.aspose.words.net.system.data/constraint)在指定索引处。
### get(String name) {#get-java.lang.String-}
```
public System.Data.Constraint get(String name)
```


获取[Constraint](../../com.aspose.words.net.system.data/constraint)从具有指定名称的集合中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 这[Constraint.getConstraintName()](../../com.aspose.words.net.system.data/constraint\#getConstraintName--) / [Constraint.setConstraintName(java.lang.String)](../../com.aspose.words.net.system.data/constraint\#setConstraintName-java.lang.String-)要返回的约束。 |

**退货:**
[Constraint](../../com.aspose.words.net.system.data/constraint) - 这[Constraint](../../com.aspose.words.net.system.data/constraint)具有指定名称；否则为空值，如果[Constraint](../../com.aspose.words.net.system.data/constraint)不存在。
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


获取集合中元素的总数。

**退货:**
int - 集合中的元素总数。
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




### remove(System.Data.Constraint constraint) {#remove-com.aspose.words.net.System.Data.Constraint-}
```
public void remove(System.Data.Constraint constraint)
```


删除指定的[Constraint](../../com.aspose.words.net.system.data/constraint)从收藏。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| constraint | [Constraint](../../com.aspose.words.net.system.data/constraint) | 这[Constraint](../../com.aspose.words.net.system.data/constraint)去除。 |

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
