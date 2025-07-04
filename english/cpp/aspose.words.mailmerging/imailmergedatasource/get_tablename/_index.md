---
title: Aspose::Words::MailMerging::IMailMergeDataSource::get_TableName method
linktitle: get_TableName
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MailMerging::IMailMergeDataSource::get_TableName method. Returns the name of the data source in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.mailmerging/imailmergedatasource/get_tablename/
---
## IMailMergeDataSource::get_TableName method


Returns the name of the data source.

```cpp
virtual System::String Aspose::Words::MailMerging::IMailMergeDataSource::get_TableName()=0
```


### ReturnValue

The name of the data source. Empty string if the data source has no name.
## Remarks


If you are implementing [IMailMergeDataSource](../), return the name of the data source from this property.

Aspose.Words uses this name to match against the mail merge region name specified in the template document. The comparison between the data source name and the mail merge region name is not case sensitive.

## See Also

* Interface [IMailMergeDataSource](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
