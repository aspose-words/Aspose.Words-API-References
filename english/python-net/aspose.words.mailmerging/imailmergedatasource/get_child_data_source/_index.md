---
title: IMailMergeDataSource.get_child_data_source method
linktitle: get_child_data_source method
articleTitle: get_child_data_source method
second_title: Aspose.Words for Python
description: "IMailMergeDataSource.get_child_data_source method. The Aspose.Words mail merge engine invokes this method when it encounters a beginning of a nested mail merge region."
type: docs
weight: 20
url: /python-net/aspose.words.mailmerging/imailmergedatasource/get_child_data_source/
---

## get_child_data_source(table_name) {#str}

The Aspose.Words mail merge engine invokes this method when it encounters a beginning of a nested mail merge region.


```python
def get_child_data_source(self, table_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| table_name | str | The name of the mail merge region as specified in the template document. Case-insensitive. |

### Remarks

When the Aspose.Words mail merge engines populates a mail merge region with data and encounters the beginning of a nested
mail merge region in the form of MERGEFIELD TableStart:TableName, it invokes [IMailMergeDataSource.get_child_data_source()](./#str) on the current
data source object. Your implementation needs to return a new data source object that will provide access to the child
records of the current parent record. Aspose.Words will use the returned data source to populate the nested mail merge region.


Below are the rules that the implementation of [IMailMergeDataSource.get_child_data_source()](./#str) must follow.


If the table that is represented by this data source object has a related child (detail) table with the specified name,
then your implementation needs to return a new [IMailMergeDataSource](../) object that will provide access
to the child records of the current record.

An example of this is Orders / OrderDetails relationship. Let's assume that the current [IMailMergeDataSource](../) object
represents the Orders table and it has a current order record. Next, Aspose.Words encounters "MERGEFIELD TableStart:OrderDetails"
in the document and invokes [IMailMergeDataSource.get_child_data_source()](./#str). You need to create and return a [IMailMergeDataSource](../)
object that will allow Aspose.Words to access the OrderDetails record for the current order.


If this data source object does not have a relation to the table with the specified name, then you need to return
a [IMailMergeDataSource](../) object that will provide access to all records of the specified table.


If a table with the specified name does not exist, your implementation should return ``None``.





### Returns

A data source object that will provide access to the data records of the specified table.


### See Also

* module [aspose.words.mailmerging](../../)
* class [IMailMergeDataSource](../)

