---
title: Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource method
linktitle: GetDataSource
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource method. The Aspose.Words mail merge engine invokes this method when it encounters a beginning of a top-level mail merge region in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/
---
## IMailMergeDataSourceRoot::GetDataSource method


The Aspose.Words mail merge engine invokes this method when it encounters a beginning of a top-level mail merge region.

```cpp
virtual System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource(System::String tableName)=0
```


| Parameter | Type | Description |
| --- | --- | --- |
| tableName | System::String | The name of the mail merge region as specified in the template document. Case-insensitive. |

### ReturnValue

A data source object that will provide access to the data records of the specified table.
## Remarks


When the Aspose.Words mail merge engines populates a document with data and encounters MERGEFIELD TableStart:TableName, it invokes [GetDataSource()](./) on this object. Your implementation needs to return a new data source object. Aspose.Words will use the returned data source to populate the mail merge region.

If a data source (table) with the specified name does not exist, your implementation should return **null**.

## See Also

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Interface [IMailMergeDataSourceRoot](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
