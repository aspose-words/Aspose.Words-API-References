---
title: IDataReader
linktitle: IDataReader
second_title: Aspose.Words for Java
description: Provides a means of reading one or more forward-only streams of result sets obtained by executing a command at a data source and is implemented by .NET Framework data providers that access relational databases in Java.
type: docs
weight: 34
url: /java/com.aspose.words.net.system.data/idatareader/
---

**All Implemented Interfaces:**
[com.aspose.words.net.System.Data.IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
```
public interface IDataReader extends System.Data.IDataRecord
```

Provides a means of reading one or more forward-only streams of result sets obtained by executing a command at a data source, and is implemented by .NET Framework data providers that access relational databases.
## Methods

| Method | Description |
| --- | --- |
| [close()](#close) | Closes the [IDataReader](../../com.aspose.words.net.system.data/idatareader/) Object. |
| [getDepth()](#getDepth) | Gets a value indicating the depth of nesting for the current row. |
| [getRecordsAffected()](#getRecordsAffected) | Gets the number of rows changed, inserted, or deleted by execution of the SQL statement. |
| [getSchemaTable()](#getSchemaTable) | Returns a [DataTable](../../com.aspose.words.net.system.data/datatable/) that describes the column metadata of the [IDataReader](../../com.aspose.words.net.system.data/idatareader/). |
| [isClosed()](#isClosed) | Gets a value indicating whether the data reader is closed. |
| [nextResult()](#nextResult) | Advances the data reader to the next result, when reading the results of batch SQL statements. |
| [read()](#read) | Advances the [IDataReader](../../com.aspose.words.net.system.data/idatareader/) to the next record. |
### close() {#close}
```
public abstract void close()
```


Closes the [IDataReader](../../com.aspose.words.net.system.data/idatareader/) Object.

### getDepth() {#getDepth}
```
public abstract int getDepth()
```


Gets a value indicating the depth of nesting for the current row.

**Returns:**
int - The level of nesting.
### getRecordsAffected() {#getRecordsAffected}
```
public abstract int getRecordsAffected()
```


Gets the number of rows changed, inserted, or deleted by execution of the SQL statement.

**Returns:**
int - The number of rows changed, inserted, or deleted; 0 if no rows were affected or the statement failed; and -1 for SELECT statements.
### getSchemaTable() {#getSchemaTable}
```
public abstract System.Data.DataTable getSchemaTable()
```


Returns a [DataTable](../../com.aspose.words.net.system.data/datatable/) that describes the column metadata of the [IDataReader](../../com.aspose.words.net.system.data/idatareader/).

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that describes the column metadata.
### isClosed() {#isClosed}
```
public abstract boolean isClosed()
```


Gets a value indicating whether the data reader is closed.

**Returns:**
boolean - true if the data reader is closed; otherwise, false.
### nextResult() {#nextResult}
```
public abstract boolean nextResult()
```


Advances the data reader to the next result, when reading the results of batch SQL statements.

**Returns:**
boolean - true if there are more rows; otherwise, false.
### read() {#read}
```
public abstract boolean read()
```


Advances the [IDataReader](../../com.aspose.words.net.system.data/idatareader/) to the next record.

**Returns:**
boolean - true if there are more rows; otherwise, false.
