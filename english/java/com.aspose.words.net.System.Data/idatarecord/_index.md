---
title: IDataRecord
linktitle: IDataRecord
second_title: Aspose.Words for Java
description: Provides access to the column values within each row for a DataReader and is implemented by .NET Framework data providers that access relational databases in Java.
type: docs
weight: 35
url: /java/com.aspose.words.net.system.data/idatarecord/
---
```
public interface IDataRecord
```

Provides access to the column values within each row for a DataReader, and is implemented by .NET Framework data providers that access relational databases.
## Methods

| Method | Description |
| --- | --- |
| [get(int i)](#get-int) | Gets the column located at the specified index. |
| [getFieldCount()](#getFieldCount) | Gets the number of columns in the current row. |
| [getFieldType(int i)](#getFieldType-int) | Gets the java.lang.Class information corresponding to the type of java.lang.Object that would be returned from [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int). |
| [getName(int i)](#getName-int) | Gets the name for the field to find. |
| [getValue(int i)](#getValue-int) | Return the value of the specified field. |
### get(int i) {#get-int}
```
public abstract Object get(int i)
```


Gets the column located at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| i | int | The zero-based index of the column to get. |

**Returns:**
java.lang.Object - The column located at the specified index as an java.lang.Object.
### getFieldCount() {#getFieldCount}
```
public abstract int getFieldCount()
```


Gets the number of columns in the current row.

**Returns:**
int - When not positioned in a valid recordset, 0; otherwise, the number of columns in the current record. The default is -1.
### getFieldType(int i) {#getFieldType-int}
```
public abstract Class getFieldType(int i)
```


Gets the java.lang.Class information corresponding to the type of java.lang.Object that would be returned from [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| i | int | The index of the field to find. |

**Returns:**
java.lang.Class - The java.lang.Class information corresponding to the type of java.lang.Object that would be returned from [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int).
### getName(int i) {#getName-int}
```
public abstract String getName(int i)
```


Gets the name for the field to find.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| i | int | The index of the field to find. |

**Returns:**
java.lang.String - The name of the field or the empty string (""), if there is no value to return.
### getValue(int i) {#getValue-int}
```
public abstract Object getValue(int i)
```


Return the value of the specified field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| i | int | The index of the field to find. |

**Returns:**
java.lang.Object - The java.lang.Object which will contain the field value upon return.
