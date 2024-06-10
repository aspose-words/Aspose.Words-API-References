---
title: IMailMergeDataSource class
linktitle: IMailMergeDataSource class
articleTitle: IMailMergeDataSource class
second_title: Aspose.Words for Python
description: "aspose.words.mailmerging.IMailMergeDataSource class. Implement this interface to allow mail merge from a custom data source, such as a list of objects"
type: docs
weight: 50
url: /python-net/aspose.words.mailmerging/imailmergedatasource/
---

## IMailMergeDataSource class

Implement this interface to allow mail merge from a custom data source, such as a list of objects. Master-detail data is also supported.


### Remarks

When a data source is created, it should be initialized to point to BOF (before the first record).
The Aspose.Words mail merge engine will invoke [IMailMergeDataSource.move_next()](./move_next/#default) to advance to next record and
then invoke [IMailMergeDataSource.get_value()](./get_value/#str_object) for every merge field it encounters in the document or the current mail merge region.




### Properties

| Name | Description |
| --- | --- |
| [table_name](./table_name/) | Returns the name of the data source. |

### Methods

| Name | Description |
| --- | --- |
|[ get_child_data_source(table_name)](./get_child_data_source/#str) | The Aspose.Words mail merge engine invokes this method when it encounters a beginning of a nested mail merge region. |
|[ get_value(field_name, field_value)](./get_value/#str_object) | Returns a value for the specified field name or ``False`` if the field is not found. |
|[ move_next()](./move_next/#default) | Advances to the next record in the data source. |

### See Also

* module [aspose.words.mailmerging](../)
* class [MailMerge](../mailmerge/)

