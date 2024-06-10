---
title: FieldMergingArgs class
linktitle: FieldMergingArgs class
articleTitle: FieldMergingArgs class
second_title: Aspose.Words for Python
description: "aspose.words.mailmerging.FieldMergingArgs class. Provides data for the MergeField event"
type: docs
weight: 10
url: /python-net/aspose.words.mailmerging/fieldmergingargs/
---

## FieldMergingArgs class

Provides data for the **MergeField** event.
To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/python-net/mail-merge-and-reporting/) documentation article.




### Remarks

The **MergeField** event occurs during mail merge when a simple mail merge
field is encountered in the document. You can respond to this event to return
text for the mail merge engine to insert into the document.




**Inheritance:** [FieldMergingArgs](./) → [FieldMergingArgsBase](../fieldmergingargsbase/)

### Properties

| Name | Description |
| --- | --- |
| [document](../fieldmergingargsbase/document/) | Returns the [FieldMergingArgsBase.document](../fieldmergingargsbase/document/) object for which the mail merge is performed.<br>(Inherited from [FieldMergingArgsBase](../fieldmergingargsbase/)) |
| [document_field_name](../fieldmergingargsbase/document_field_name/) | Gets the name of the merge field as specified in the document.<br>(Inherited from [FieldMergingArgsBase](../fieldmergingargsbase/)) |
| [field](../fieldmergingargsbase/field/) | Gets the object that represents the current merge field.<br>(Inherited from [FieldMergingArgsBase](../fieldmergingargsbase/)) |
| [field_name](../fieldmergingargsbase/field_name/) | Gets the name of the merge field in the data source.<br>(Inherited from [FieldMergingArgsBase](../fieldmergingargsbase/)) |
| [field_value](../fieldmergingargsbase/field_value/) | Gets or sets the value of the field from the data source.<br>(Inherited from [FieldMergingArgsBase](../fieldmergingargsbase/)) |
| [record_index](../fieldmergingargsbase/record_index/) | Gets the zero based index of the record that is being merged.<br>(Inherited from [FieldMergingArgsBase](../fieldmergingargsbase/)) |
| [table_name](../fieldmergingargsbase/table_name/) | Gets the name of the data table for the current merge operation or empty string if the name is not available.<br>(Inherited from [FieldMergingArgsBase](../fieldmergingargsbase/)) |
| [text](./text/) | Gets or sets the text that will be inserted into the document for the current merge field. |

### See Also

* module [aspose.words.mailmerging](../)
* class [FieldMergingArgsBase](../fieldmergingargsbase/)
* class [IFieldMergingCallback](../ifieldmergingcallback/)

