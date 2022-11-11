---
title: DbDataReader
second_title: Aspose.Words for Java API Reference
description: 从数据源读取只进的行流。
type: docs
weight: 10
url: /zh/java/com.aspose.words.net.system.data.common/dbdatareader/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
[com.aspose.words.net.System.Data.IDataReader](../../com.aspose.words.net.system.data/idatareader), [com.aspose.words.net.System.Data.IDataRecord](../../com.aspose.words.net.system.data/idatarecord), java.lang.Iterable
```
public abstract class DbDataReader implements System.Data.IDataReader, System.Data.IDataRecord, Iterable
```

从数据源读取只进的行流。
## 构造函数s

| 构造函数 | 描述 |
| --- | --- |
| [DbDataReader()](#DbDataReader--) |  |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(String columnName)](#get-java.lang.String-) | 此方法属于 .NET 中的 IDataRecord |
| [get班级()](#get班级--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DbDataReader() {#DbDataReader--}
```
public DbDataReader()
```


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
### get(String columnName) {#get-java.lang.String-}
```
public abstract Object get(String columnName)
```


此方法属于 .NET 中的 IDataRecord

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| columnName | java.lang.String |  |

**退货:**
java.lang.Object
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
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
