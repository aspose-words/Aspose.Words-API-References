---
title: MailMerge.execute_with_regions method
linktitle: execute_with_regions method
articleTitle: execute_with_regions method
second_title: Aspose.Words for Python
description: "aspose.words.mailmerging.MailMerge.execute_with_regions method"
type: docs
weight: 190
url: /python-net/aspose.words.mailmerging/mailmerge/execute_with_regions/
---

## execute_with_regions(data_source) {#imailmergedatasource}

Performs a mail merge from a custom data source with mail merge regions.


```python
def execute_with_regions(self, data_source: aspose.words.mailmerging.IMailMergeDataSource):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| data_source | [IMailMergeDataSource](../../imailmergedatasource/) | An object that implements the custom mail merge data source interface. |

### Remarks

Use this method to fill mail merge fields in the document with values from
any custom data source such as an XML file or collections of business objects. You need to write your
own class that implements the [IMailMergeDataSource](../../imailmergedatasource/) interface.

You can use this method only when [FieldOptions.is_bidi_text_supported_on_update](../../../aspose.words.fields/fieldoptions/is_bidi_text_supported_on_update/) is ``False``,
that is you do not need Right-To-Left language (such as Arabic or Hebrew) compatibility.




## execute_with_regions(data_source_root) {#imailmergedatasourceroot}

Performs a mail merge from a custom data source with mail merge regions.


```python
def execute_with_regions(self, data_source_root: aspose.words.mailmerging.IMailMergeDataSourceRoot):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| data_source_root | [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/) | An object that implements the custom mail merge data source root interface. |

### Remarks

Use this method to fill mail merge fields in the document with values from
any custom data source such as an XML file or collections of business objects. You need to write your own classes
that implement the [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/) and [IMailMergeDataSource](../../imailmergedatasource/) interfaces.

You can use this method only when [FieldOptions.is_bidi_text_supported_on_update](../../../aspose.words.fields/fieldoptions/is_bidi_text_supported_on_update/) is ``False``,
that is you do not need Right-To-Left language (such as Arabic or Hebrew) compatibility.




## See Also

* module [aspose.words.mailmerging](../../)
* class [MailMerge](../)

