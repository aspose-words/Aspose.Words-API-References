---
title: IMailMergeDataSourceRoot.get_data_source method
linktitle: get_data_source method
articleTitle: get_data_source method
second_title: Aspose.Words for Python
description: "IMailMergeDataSourceRoot.get_data_source method. The Aspose.Words mail merge engine invokes this method when it encounters a beginning of a top-level mail merge region."
type: docs
weight: 10
url: /python-net/aspose.words.mailmerging/imailmergedatasourceroot/get_data_source/
---

## get_data_source(table_name) {#str}

The Aspose.Words mail merge engine invokes this method when it encounters a beginning of a top-level mail merge region.


```python
def get_data_source(self, table_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| table_name | str | The name of the mail merge region as specified in the template document. Case-insensitive. |

### Remarks

When the Aspose.Words mail merge engines populates a document with data and encounters MERGEFIELD TableStart:TableName,
it invokes [IMailMergeDataSourceRoot.get_data_source()](./#str) on this object. Your implementation needs to return a new data source object.
Aspose.Words will use the returned data source to populate the mail merge region.


If a data source (table) with the specified name does not exist, your implementation should return ``None``.





### Returns

A data source object that will provide access to the data records of the specified table.


### See Also

* module [aspose.words.mailmerging](../../)
* class [IMailMergeDataSourceRoot](../)

