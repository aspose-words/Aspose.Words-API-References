---
title: IMailMergeDataSource
second_title: Aspose.Words for Java API Reference
description: Implement this interface to allow mail merge from a custom data source such as a list of objects.
type: docs
weight: 650
url: /java/com.aspose.words/imailmergedatasource/
---
```
public interface IMailMergeDataSource
```

Implement this interface to allow mail merge from a custom data source, such as a list of objects. Master-detail data is also supported.

When a data source is created, it should be initialized to point to BOF (before the first record). The Aspose.Words mail merge engine will invoke [moveNext()](../../com.aspose.words/imailmergedatasource\#moveNext--) to advance to next record and then invoke **M:Aspose.Words.MailMerging.IMailMergeDataSource.GetValue(System.String,System.Object@)** for every merge field it encounters in the document or the current mail merge region.
## Methods

| Method | Description |
| --- | --- |
| [getTableName()](#getTableName--) | Returns the name of the data source. |
| [moveNext()](#moveNext--) | Advances to the next record in the data source. |
| [getValue(String fieldName, Ref fieldValue)](#getValue-java.lang.String-com.aspose.words.ref.Ref-) |  |
| [getChildDataSource(String tableName)](#getChildDataSource-java.lang.String-) | The Aspose.Words mail merge engine invokes this method when it encounters a beginning of a nested mail merge region. |
### getTableName() {#getTableName--}
```
public abstract String getTableName()
```


Returns the name of the data source.

If you are implementing [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource), return the name of the data source from this property.

Aspose.Words uses this name to match against the mail merge region name specified in the template document. The comparison between the data source name and the mail merge region name is not case sensitive.

**Returns:**
java.lang.String - The name of the data source. Empty string if the data source has no name.
### moveNext() {#moveNext--}
```
public abstract boolean moveNext()
```


Advances to the next record in the data source.

**Returns:**
boolean - True if moved to next record successfully. False if reached end of the data source.
### getValue(String fieldName, Ref fieldValue) {#getValue-java.lang.String-com.aspose.words.ref.Ref-}
```
public abstract boolean getValue(String fieldName, Ref fieldValue)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldName | java.lang.String |  |
| fieldValue | [Ref](../../com.aspose.words.ref/ref) |  |

**Returns:**
boolean
### getChildDataSource(String tableName) {#getChildDataSource-java.lang.String-}
```
public abstract IMailMergeDataSource getChildDataSource(String tableName)
```


The Aspose.Words mail merge engine invokes this method when it encounters a beginning of a nested mail merge region.

When the Aspose.Words mail merge engines populates a mail merge region with data and encounters the beginning of a nested mail merge region in the form of MERGEFIELD TableStart:TableName, it invokes [getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource\#getChildDataSource-java.lang.String-) on the current data source object. Your implementation needs to return a new data source object that will provide access to the child records of the current parent record. Aspose.Words will use the returned data source to populate the nested mail merge region.

Below are the rules that the implementation of [getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource\#getChildDataSource-java.lang.String-) must follow.

If the table that is represented by this data source object has a related child (detail) table with the specified name, then your implementation needs to return a new [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource) object that will provide access to the child records of the current record. An example of this is Orders / OrderDetails relationship. Let's assume that the current [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource) object represents the Orders table and it has a current order record. Next, Aspose.Words encounters "MERGEFIELD TableStart:OrderDetails" in the document and invokes [getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource\#getChildDataSource-java.lang.String-). You need to create and return a [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource) object that will allow Aspose.Words to access the OrderDetails record for the current order.

If this data source object does not have a relation to the table with the specified name, then you need to return a [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource) object that will provide access to all records of the specified table.

If a table with the specified name does not exist, your implementation should return  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tableName | java.lang.String | The name of the mail merge region as specified in the template document. Case-insensitive. |

**Returns:**
[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource) - A data source object that will provide access to the data records of the specified table.
