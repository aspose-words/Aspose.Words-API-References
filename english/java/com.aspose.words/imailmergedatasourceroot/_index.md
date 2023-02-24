---
title: IMailMergeDataSourceRoot
linktitle: IMailMergeDataSourceRoot
second_title: Aspose.Words for Java API Reference
description: Implement this interface to allow mail merge from a custom data source with master-detail data in Java.
type: docs
weight: 658
url: /java/com.aspose.words/imailmergedatasourceroot/
---
```
public interface IMailMergeDataSourceRoot
```

Implement this interface to allow mail merge from a custom data source with master-detail data.
## Methods

| Method | Description |
| --- | --- |
| [getDataSource(String tableName)](#getDataSource-java.lang.String) | The Aspose.Words mail merge engine invokes this method when it encounters a beginning of a top-level mail merge region. |
### getDataSource(String tableName) {#getDataSource-java.lang.String}
```
public abstract IMailMergeDataSource getDataSource(String tableName)
```


The Aspose.Words mail merge engine invokes this method when it encounters a beginning of a top-level mail merge region.

When the Aspose.Words mail merge engines populates a document with data and encounters MERGEFIELD TableStart:TableName, it invokes [getDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasourceroot/\#getDataSource-java.lang.String) on this object. Your implementation needs to return a new data source object. Aspose.Words will use the returned data source to populate the mail merge region.

If a data source (table) with the specified name does not exist, your implementation should return  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tableName | java.lang.String | The name of the mail merge region as specified in the template document. Case-insensitive. |

**Returns:**
[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) - A data source object that will provide access to the data records of the specified table.
