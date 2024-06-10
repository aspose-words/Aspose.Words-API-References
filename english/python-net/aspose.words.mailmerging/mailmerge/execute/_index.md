---
title: MailMerge.execute method
linktitle: execute method
articleTitle: execute method
second_title: Aspose.Words for Python
description: "aspose.words.mailmerging.MailMerge.execute method"
type: docs
weight: 180
url: /python-net/aspose.words.mailmerging/mailmerge/execute/
---

## execute(data_source) {#imailmergedatasource}

Performs a mail merge from a custom data source.


```python
def execute(self, data_source: aspose.words.mailmerging.IMailMergeDataSource):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| data_source | [IMailMergeDataSource](../../imailmergedatasource/) | An object that implements the custom mail merge data source interface. |

### Remarks

Use this method to fill mail merge fields in the document with values from
any data source such as a list or hashtable or objects. You need to write your
own class that implements the [IMailMergeDataSource](../../imailmergedatasource/) interface.

You can use this method only when [FieldOptions.is_bidi_text_supported_on_update](../../../aspose.words.fields/fieldoptions/is_bidi_text_supported_on_update/) is ``False``,
that is you do not need Right-To-Left language (such as Arabic or Hebrew) compatibility.

This method ignores the [MailMergeCleanupOptions.REMOVE_UNUSED_REGIONS](../../mailmergecleanupoptions/#REMOVE_UNUSED_REGIONS) option.




## execute(field_names, values) {#strlist_objectlist}

Performs a mail merge operation for a single record.


```python
def execute(self, field_names: List[str], values: List[object]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| field_names | List[str] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| values | List[object] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in *fieldNames*. |

### Remarks

Use this method to fill mail merge fields in the document with values from
an array of objects.

This method merges data for one record only. The array of field names
and the array of values represent the data of a single record.

This method does not use mail merge regions.

This method ignores the [MailMergeCleanupOptions.REMOVE_UNUSED_REGIONS](../../mailmergecleanupoptions/#REMOVE_UNUSED_REGIONS) option.




## See Also

* module [aspose.words.mailmerging](../../)
* class [MailMerge](../)

