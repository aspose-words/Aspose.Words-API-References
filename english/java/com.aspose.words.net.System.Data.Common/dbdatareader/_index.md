---
title: DbDataReader
second_title: Aspose.Words for Java API Reference
description: Reads a forward-only stream of rows from a data source.
type: docs
weight: 10
url: /java/com.aspose.words.net.system.data.common/dbdatareader/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.net.System.Data.IDataReader](../../com.aspose.words.net.system.data/idatareader), [com.aspose.words.net.System.Data.IDataRecord](../../com.aspose.words.net.system.data/idatarecord), java.lang.Iterable
```
public abstract class DbDataReader implements System.Data.IDataReader, System.Data.IDataRecord, Iterable
```

Reads a forward-only stream of rows from a data source.
## Constructors

| Constructor | Description |
| --- | --- |
| [DbDataReader()](#DbDataReader--) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(String columnName)](#get-java.lang.String-) | This method belongs to IDataRecord in .NET |
| [getClass()](#getClass--) |  |
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




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### get(String columnName) {#get-java.lang.String-}
```
public abstract Object get(String columnName)
```


This method belongs to IDataRecord in .NET

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String |  |

**Returns:**
java.lang.Object
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
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




**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

