---
title: Aspose::Words::MailMerging::IMailMergeDataSource interface
linktitle: IMailMergeDataSource
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MailMerging::IMailMergeDataSource interface. Implement this interface to allow mail merge from a custom data source, such as a list of objects. Master-detail data is also supported in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.mailmerging/imailmergedatasource/
---
## IMailMergeDataSource interface


Implement this interface to allow mail merge from a custom data source, such as a list of objects. Master-detail data is also supported.

```cpp
class IMailMergeDataSource : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [GetChildDataSource](./getchilddatasource/)(System::String) | The Aspose.Words mail merge engine invokes this method when it encounters a beginning of a nested mail merge region. |
| virtual [GetValue](./getvalue/)(System::String, System::SharedPtr\<System::Object\> \&) | Returns a value for the specified field name or **false** if the field is not found. |
| virtual [MoveNext](./movenext/)() | Advances to the next record in the data source. |
| virtual [get_TableName](./get_tablename/)() | Returns the name of the data source. |
## Remarks


When a data source is created, it should be initialized to point to BOF (before the first record). The Aspose.Words mail merge engine will invoke [MoveNext](./movenext/) to advance to next record and then invoke [GetValue()](./getvalue/) for every merge field it encounters in the document or the current mail merge region.
## See Also

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
