---
title: DataView
second_title: Aspose.Words for Java API 参考
description: 表示用于排序过滤搜索编辑和导航的数据绑定自定义视图。
type: docs
weight: 28
url: /zh/java/com.aspose.words.net.system.data/dataview/
---

**遗产：**
java.lang.Object

**所有已实现的接口：**
java.lang.Iterable
```
public class DataView implements Iterable
```

表示一个可数据绑定的自定义视图[DataTable](../../com.aspose.words.net.system.data/datatable)用于排序、过滤、搜索、编辑和导航。
## 构造器

| 构造函数 | 描述 |
| --- | --- |
| [DataView(System.Data.DataTable table)](#DataView-com.aspose.words.net.System.Data.DataTable-) | 初始化一个新的实例[DataView](../../com.aspose.words.net.system.data/dataview)类与指定[DataTable](../../com.aspose.words.net.system.data/datatable). |
## 方法

| 方法 | 描述 |
| --- | --- |
| [close()](#close--) | 关闭[DataView](../../com.aspose.words.net.system.data/dataview). |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int recordIndex)](#get-int-) | 从指定表中获取一行数据。 |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | 获取记录中的条数[DataView](../../com.aspose.words.net.system.data/dataview). |
| [getTable()](#getTable--) | 获取来源[DataTable](../../com.aspose.words.net.system.data/datatable). |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | 为此获取一个枚举器[DataView](../../com.aspose.words.net.system.data/dataview). |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DataView(System.Data.DataTable table) {#DataView-com.aspose.words.net.System.Data.DataTable-}
```
public DataView(System.Data.DataTable table)
```


初始化一个新的实例[DataView](../../com.aspose.words.net.system.data/dataview)类与指定[DataTable](../../com.aspose.words.net.system.data/datatable).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable) | 一个[DataTable](../../com.aspose.words.net.system.data/datatable)添加到[DataView](../../com.aspose.words.net.system.data/dataview). |

### close() {#close--}
```
public void close()
```


关闭[DataView](../../com.aspose.words.net.system.data/dataview).

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
### get(int recordIndex) {#get-int-}
```
public System.Data.DataRowView get(int recordIndex)
```


从指定表中获取一行数据。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| recordIndex | int | 记录中的索引[DataTable](../../com.aspose.words.net.system.data/datatable). |

**退货：**
[DataRowView](../../com.aspose.words.net.system.data/datarowview) - 一个[DataRowView](../../com.aspose.words.net.system.data/datarowview)你想要的行。
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


获取记录中的条数[DataView](../../com.aspose.words.net.system.data/dataview).

**退货：**
 int - 中的记录数[DataView](../../com.aspose.words.net.system.data/dataview).
### getTable() {#getTable--}
```
public System.Data.DataTable getTable()
```


获取来源[DataTable](../../com.aspose.words.net.system.data/datatable).

**退货：**
[DataTable](../../com.aspose.words.net.system.data/datatable) - 一个[DataTable](../../com.aspose.words.net.system.data/datatable)为该视图提供数据。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### iterator() {#iterator--}
```
public Iterator iterator()
```


为此获取一个枚举器[DataView](../../com.aspose.words.net.system.data/dataview).

**退货：**
java.util.Iterator - 用于在列表中导航的 java.util.Iterator。
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
