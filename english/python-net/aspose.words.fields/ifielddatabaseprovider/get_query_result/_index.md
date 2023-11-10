---
title: IFieldDatabaseProvider.get_query_result method
linktitle: get_query_result method
articleTitle: get_query_result method
second_title: Aspose.Words for Python
description: "IFieldDatabaseProvider.get_query_result method. Returns query result."
type: docs
weight: 10
url: /python-net/aspose.words.fields/ifielddatabaseprovider/get_query_result/
---

## get_query_result(file_name, connection, query, field) {#str_str_str_fielddatabase}

Returns query result.


```python
def get_query_result(self, file_name: str, connection: str, query: str, field: aspose.words.fields.FieldDatabase):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | The complete path and file name of the database specified in the \\d field switch. |
| connection | str | The connection to the data specified in the \\c field switch. |
| query | str | The set of SQL instructions that query the database specified in the \\s field switch. |
| field | [FieldDatabase](../../fielddatabase/) | The field being updated. |

### Returns

The [FieldDatabaseDataTable](../../fielddatabasedatatable/) instance that should be used for the field's update.


### See Also

* module [aspose.words.fields](../../)
* class [IFieldDatabaseProvider](../)

