---
title: Aspose::Words::Settings::MailMergeDestination enum
linktitle: MailMergeDestination
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Settings::MailMergeDestination enum. Specifies the possible results which may be generated when a mail merge is carried out on a document in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words.settings/mailmergedestination/
---
## MailMergeDestination enum


Specifies the possible results which may be generated when a mail merge is carried out on a document.

```cpp
enum class MailMergeDestination
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| NewDocument | 0 | Specifies that conforming hosting applications shall generate new documents by populating the fields within a given document with data from the specified external data source. |
| Printer | 1 | Specifies that conforming hosting applications shall print the documents that result from populating the fields within a given document with external data from the specified external data source. |
| Email | 2 | Specifies that conforming hosting applications shall generate emails using the documents that result from populating the fields within a given document with data from the specified external data source. |
| Fax | 4 | Specifies that conforming hosting applications shall generate faxes using the documents that result from populating the fields within a given document with data from the specified external data source. |
| Default | n/a | Equals to the [NewDocument](./) value. |


## See Also

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
