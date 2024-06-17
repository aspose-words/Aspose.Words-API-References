---
title: IFieldDatabaseProvider
linktitle: IFieldDatabaseProvider
second_title: Aspose.Words for Java
description: Implement this interface to provide data for the FieldDatabase field when its updated in Java.
type: docs
weight: 696
url: /java/com.aspose.words/ifielddatabaseprovider/
---
```
public interface IFieldDatabaseProvider
```

Implement this interface to provide data for the [FieldDatabase](../../com.aspose.words/fielddatabase/) field when it's updated.
## Methods

| Method | Description |
| --- | --- |
| [getQueryResult(String fileName, String connection, String query, FieldDatabase field)](#getQueryResult-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.FieldDatabase) | Returns query result. |
### getQueryResult(String fileName, String connection, String query, FieldDatabase field) {#getQueryResult-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.FieldDatabase}
```
public abstract FieldDatabaseDataTable getQueryResult(String fileName, String connection, String query, FieldDatabase field)
```


Returns query result.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The complete path and file name of the database specified in the \\d field switch. |
| connection | java.lang.String | The connection to the data specified in the \\c field switch. |
| query | java.lang.String | The set of SQL instructions that query the database specified in the \\s field switch. |
| field | [FieldDatabase](../../com.aspose.words/fielddatabase/) | The field being updated. |

**Returns:**
[FieldDatabaseDataTable](../../com.aspose.words/fielddatabasedatatable/) - The [FieldDatabaseDataTable](../../com.aspose.words/fielddatabasedatatable/) instance that should be used for the field's update.
